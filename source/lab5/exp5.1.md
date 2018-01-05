ELEC 243 Lab

------------------------------------------------------------------------

Experiment 5.1
--------------

The 741 Op-Amp
--------------

### Components

-   741 Op Amp
-   Resistors: 1-10 ![\$\\Omega\$](img8.png){width="15" height="14"} ,
    1-10 k![\$\\Omega\$](img8.png){width="15" height="14"}

The 741 operational amplifier, or op-amp, comes in an 8-pin dual inline
package (DIP) which looks like this

![](../figs/741_photo2.jpg)

If you look closely at the package, you will find a notch at one end or
a dot in one corner. This tells us how to find Pin 1: the dot is located
next to Pin 1 and the notch is located between Pins 1 and 8. The rest of
the pins are numbered like this:

![](../figs/741_pkg.gif){width="300"}

Pin 8 is not connected (NC). Pins 1 and 5 are used to eliminate the
offset voltage. We won't be using this feature this week, so don't
connect anything to these pins. The remaining pins give us the following
circuit symbol for our op-amp:

![\\includegraphics\[scale=0.640000\]{opamps/cktsym.ps}](img232.png){width="267"
height="135"}

For more information, see the [741 data
sheet](http://www.ti.com/lit/ds/symlink/lm741.pdf).

In order to function, the op-amp must be connected to an external *power
supply*. Since we want to produce both positive and negative output
voltages, we need both positive and negative voltages for the power
supply. These are labeled ![\$V\_{CC+}\$](img48.png){width="43"
height="30"} and ![\$V\_{CC-}\$](img49.png){width="43" height="30"} on
the diagram. For a 741, the nominal values are
![\$V\_{CC+}\$](img48.png){width="43" height="30"} =15 V and
![\$V\_{CC-}\$](img49.png){width="43" height="30"} =15 V.

To avoid clutter, we won't show the power supply terminals (pins 4 and
7) on any of the subsequent circuit diagrams. However, they must be
connected or your amplifier will not operate.

Note that there is no ground terminal on the op-amp. The zero reference
point is established by the external circuit and is not important to the
op-amp itself.

### Part A: Powering up the Op-Amp

- If you have not already done so, wire the bus strips on your
breadboard (as described in the [Prelude](file.27.html) section) to
provide positive power, negative power and ground buses.

- Plug an op-amp into the breadboard so that it straddles the gap
between the top and bottom sections of the socket strip. If you have
wired the power buses as suggested above, Pin 1 should be to the left.\
![](../figs/dot_clear.gif)\

  ------------------------------------------------------------------------
  **Warning**
  Do not try to unplug the op-amp with your thumb and forefinger. It's a
  good way to end up with the op-amp plugged into your fingertip. Use the
  pliers or [IC puller](../figs/ic_puller.jpg) from your toolkit.
  ------------------------------------------------------------------------

- Connect Pin 4 (![\$V\_{CC-}\$](img49.png){width="43" height="30"} ) to
the negative power supply bus (-15 V). Connect Pin 7
(![\$V\_{CC+}\$](img48.png){width="43" height="30"} ) to the positive
power supply bus (+15 V).

![](../figs/opamp_pwr.jpg)

- With the power supply off, adjust the +25V supply to 15V and -25V to
-15V.

- Connect the negative power supply to the black banana jack on your
breadboard, the positive power supply to the red breadboard banana jack,
and the common (arrow) terminal to the green breadboard banana jack. The
common terminal must now be grounded, so use a fourth banana plug cable
to connect the common terminal to the ground terminal on the power
supply dongle.

### Part B: Open-Loop Response

- Caution: The components we've used so far have been simple (only two
terminals) and fairly rugged (connecting a resistor "backwards" won't
harm it). The op-amp has four times as many pins, so it's easier to make
a mistake in wiring it. Unfortunately, it's also considerably more
delicate, so connecting it incorrectly can destroy it.

The moral: Always wire your circuit with the power turned off and check
your wiring carefully before turning the power on.

- With the power turned off, wire the following circuit. Note that this
is a 1000:1 voltage divider, so that a 1 V signal at
![\$v\_{in}\$](img50.png){width="24" height="29"} results in a 1 mV
signal at the input of the op-amp.
![\\includegraphics\[scale=0.650000\]{opamps/open\_loop.ps}](img233.png){width="390"
height="114"}

- In the experiments below we will see the shortcomings of a real (as
opposed to an ideal) operational amplifier. **As you go through the
experiments below, explain in your report which experiments demonstrate
the following:** (1) clipping, which limits the maximum amplitude of the
output; (2) slew-rate limitation, which limits the maximum slope of the
output; (3) offset, which gives a non-zero output for zero input.

- Set the function generator to produce a 2 V p-p, 20 Hz sine wave.

- Connect the function generator output to
![\$v\_{in}\$](img50.png){width="24" height="29"} of the circuit above.
Connect `CH1` of the scope to ![\$v\_{in}\$](img50.png){width="24"
height="29"} and `CH2` to ![\$v\_{out}\$](img51.png){width="30"
height="29"} . Make sure both channels of the scope are on `DC`.

- You should see a badly distorted (clipped) waveform at
![\$v\_{out}\$](img51.png){width="30" height="29"} . If you don't, try
increasing the function generator output.**Take a screenshot for your
lab report and note your vin value. Why is the output distorted?**

- Adjust DC offset on the function generator until the waveform is
roughly a symmetrical square wave. **Note the positive and negative peak
values of ![\$v\_{out}\$](img51.png){width="30" height="29"}. What is
the DC offset value that was required to get symmetrical output?**

- Connect a 100![\$\\Omega\$](img8.png){width="15" height="14"} resistor
from ![\$v\_{out}\$](img51.png){width="30" height="29"} to ground.
**What happens to the output signal?**

- Remove the 100![\$\\Omega\$](img8.png){width="15" height="14"}
resistor from the op-amp output. Set the function generator output to
square wave. **Note the shape of the
![\$v\_{out}\$](img51.png){width="30" height="29"} waveform. Is the
output able to switch as fast as the fast-switching square wave input?**

- Set the function generator to produce a 1 kHz sine wave. Adjust the
amplitude and DC offset until the op-amp output is a 10 V p-p unclipped
sine wave. **Note the amplitude of the function generator output. Can
you estimate the open-loop gain of your opamp? Is it consistent with the
specifications in the data sheet? (Look up the large signal voltage
gain).**

- When we reduce the overall gain with feedback, some of these (e.g.
offset) are reduced significantly, and we get an output which is an
amplified version of the input. However, other limits (such as maximum
output) appear.
