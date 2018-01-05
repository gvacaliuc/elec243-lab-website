ELEC 243 Lab

------------------------------------------------------------------------

Experiment 5.2
--------------

Voltage Amplifiers
------------------

### Components

-   741 Op Amp
-   Resistors: 1-100 ![\$\\Omega\$](img8.png){width="15" height="14"} ,
    2-10 k![\$\\Omega\$](img8.png){width="15" height="14"} ,
    1-100 k![\$\\Omega\$](img8.png){width="15" height="14"}

As we saw in the previous experiment, the op-amp isn't very useful in an
"open-loop" configuration (i.e. without feedback). The most common
configuration for op-amp circuits is the *inverting amplifier* where the
output is an amplified and inverted version of the input (i.e.
![\$A\$](img26.png){width="15" height="14"} is negative). From this
starting point we can create a number of different input-output
relationships, including sum, difference, and non-inverted gain.

### Part A: The Basic Inverting Amplifier

- Wire the following circuit using
10 k![\$\\Omega\$](img8.png){width="15" height="14"} resistors for both
![\$R\_1\$](img52.png){width="22" height="30"} and
![\$R\_F\$](img53.png){width="26" height="30"} .

![\\includegraphics\[scale=0.650000\]{../241/inv\_opamp.ps}](img234.png){width="314"
height="177"}\

Fig. 5.1: Inverting Amplifier

- Set the function generator to produce a 1 V p-p, 100 Hz sine wave.
**Measure the voltage gain**, ![\$A\_v =
\\frac{V\_{out}}{V\_{in}}\$](img54.png){width="73" height="37"} using
the oscilloscope. Note that the output is inverted with respect to the
input.

- Replace ![\$R\_F\$](img53.png){width="26" height="30"} with a
100 k![\$\\Omega\$](img8.png){width="15" height="14"} resistor.
**Measure the gain.**

- Increase the input amplitude until output clipping occurs. **What is
the clipping level? Is it the same as in Exp. 5.1?**

- Reduce the input amplitude till the output is 20 V p-p. Then increase
the frequency until the output amplitude drops to 10 V p-p. You should
see a triangular output waveform. This is because there is a limit to
the maximum rate at which the output voltage can change, called the
*slew rate.*

- Set the input to triangle and square wave and **comment on how the
output changes.**

- Reset the function generator for a 100 Hz sine wave and reduce the
amplitude to produce a 1 V p-p output from the op amp.

- Again increase the frequency until the output is 0.7 V p-p. Observe
that the output is still sinusoidal. **Note the frequency.** This is
called the cutoff frequency or *bandwidth* of the amplifier.

### Part B: Summing Amplifier

There are a number of applications where it is useful to produce the
sum, or more generally the weighted sum, of two or more signals. One
example is the mixer system in a recording or broadcast studio where
various sources (microphones, audio files, etc.) are combined to produce
the final mix for the track or program.

- The inverting amplifier configuration we used makes this very easy to
do, just add another resistor to the inverting (-) input of the op amp:

![\\includegraphics\[scale=0.650000\]{opamps/summer.ps}](img235.png){width="311"
height="173"}\

Fig. 5.2: Summing Amplifier

A quick analysis shows that ![\$v\_{out} = -(\\frac{R\_F}{R\_1}v\_1 +
\\frac{R\_F}{R\_2}v\_2)\$](img57.png){width="170" height="37"} , i.e.
the output is a weighted sum of the inputs. The key is to notice that
the current flowing in ![\$R\_F\$](img53.png){width="26" height="30"}
must be (by KCL) equal to the sum of the currents in
![\$R\_1\$](img52.png){width="22" height="30"} and
![\$R\_2\$](img58.png){width="22" height="30"} . For this reason, the
node of an op amp circuit which is connected to the inverting input is
sometimes referred to as the *summing junction*. This summation can be
extended to any number of inputs.

- Rather than just add two arbitrary signals together and watch the
result on the oscilloscope, let's do something a bit more entertaining:
add two signals together and listen to them. From our observations in
Part A of Experiment 2.2 and Part A of this Experiment, we would expect
to have trouble driving the loudspeaker with the output of the op-amp.
Fortunately, we have a more suitable acoustic output transducer: the
earpiece of the telephone handset. The telephone earpiece is also very
easy to connect to: just plug it into J1-7 and wire to the appropriate
pins on the interface module connector strip. Notice that, unlike the
microphone, neither of the two earpiece terminals is automatically
grounded. Be sure to ground one and connect the other to
![\$v\_{out}\$](img51.png){width="30" height="29"} .

- For our two inputs, we will use the function generator for
![\$v\_1\$](img59.png){width="18" height="29"} and the dynamic
microphone for ![\$v\_2\$](img60.png){width="18" height="29"} . The
earpiece produces a comfortably loud output with a signal of about
1 V p-p. This is a level easy to produce with the function generator, so
we will choose a gain of 1 from ![\$v\_1\$](img59.png){width="18"
height="29"} to ![\$v\_out\$](img60.png){width="18" height="29"} . This
means we must choose ![\$R\_1=R\_F\$](img61.png){width="66" height="30"}
, but says nothing about the actual value. From past experience, 100 kΩ
is a good choice. **Choose the value of
![\$R\_2\$](img58.png){width="22" height="30"} required to give a
1 V p-p output when speaking into the microphone in a normal tone of
voice.** (Hint: Plug in your microphone into J1-4, and view pin 4 on
your oscilloscope to see the approximate peak-to-peak output when you
speak into the microphone. Then calculate the gain required to get 1-V
output. Size R2 based on this).

- Build the circuit using the component values you determined in the
previous step. Connect ![\$v\_1\$](img59.png){width="18" height="29"} ,
![\$v\_2\$](img60.png){width="18" height="29"} , and
![\$v\_{out}\$](img51.png){width="30" height="29"} appropriately
(function generator, microphone, handset). Also connect
![\$v\_{out}\$](img51.png){width="30" height="29"} to the oscilloscope.
When the circuit is completed, speak into the microphone at a normal
speaking level and **verify that the output
![\$v\_{mic}\$](img62.png){width="33" height="29"} is approximately
1 V p-p.**

- Set the function generator to produce a 440 Hz sine wave (musical note
A). Adjust the amplitude to produce a comfortable listening level in the
handset earpiece. While listening to the earpiece and watching the
oscilloscope, hum the note A. **Take a screenshot and describe what
happens on the scope when you are in tune and when you are slightly out
of tune with the function generator.** If the range of your voice does
not encompass A440, try tuning the function generator down an octave to
220 Hz.

### Part C: Non-Inverting Amplifier

So far all of the op-amp circuits we have examined have been
*inverting*, i.e. the polarity of the output is inverted with respect to
the input. This doesn't have to be the case, as the following circuit
shows:

![\\includegraphics\[scale=0.500000\]{ckt7.1.1.ps}](img236.png){width="242"
height="167"}

Fig. 5.3: Non-inverting Amplifier

This is an example of the basic *non-inverting* op-amp configuration. A
simple analysis shows that
![\$v\_{out}=(1+\\frac{R\_2}{R\_1})v\_{in}\$](img63.png){width="132"
height="37"} (with no minus sign). This circuit has a couple of useful
characteristics. Most obvious is that it doesn't invert. Another is that
the input impedance is extremely high. One potential disadvantage is
that the minimum value of gain is unity.

- Using another 741 op amp, wire the non-inverting amplifier circuit.
Let ![\$R\_1\$](img52.png){width="22" height="30"} be 1 kΩ. Choose
![\$R\_2\$](img58.png){width="22" height="30"} to give a gain of 2.

- Connect a 1 V p-p 1 kHz sine wave to
![\$v\_{in}\$](img50.png){width="24" height="29"} . Observe
![\$v\_{in}\$](img50.png){width="24" height="29"} and
![\$v\_{out}\$](img51.png){width="30" height="29"} on the oscilloscope.

- **Take a screenshot. What is the actual gain? Is it in
non-inverting?**

### Part D: Difference Amplifier

What if we want the difference, rather than the sum of two signals? We
could combine an inverting amplifier with a summing amplifier to negate
one of the signals before forming a sum, but this would require two
op-amps. A simpler circuit results from combining an inverting and a
non-inverting configuration on the same op-amp, like this:

![\\includegraphics\[scale=0.500000\]{opamps/diff2.ps}](img237.png){width="282"
height="178"}

Fig. 5.4: Difference Amplifier

For arbitrary values of the resistors, we get ![\$\\displaystyle
v\_{out}=-\\frac{R\_2}{R\_1}v\_1+\\frac{R\_4}{R\_3+R\_4}\\frac{R\_1+R\_2}{R\_1}v\_2\$](img64.png){width="259"
height="52"} which doesn't seem very useful. However, if we let
![\$R\_3=R\_1\$](img65.png){width="63" height="30"} and
![\$R\_4=R\_2\$](img66.png){width="63" height="30"} , then we have
![\$\\displaystyle
v\_{out}=\\frac{R\_2}{R\_1}(v\_2-v\_1)\$](img67.png){width="136"
height="52"} i.e. a *difference amplifier*.

- Wire the above circuit, using 10 kΩ for all four resistors.

- Using the function generator for ![\$v\_1\$](img59.png){width="18"
height="29"} and the 0-6 V power supply for
![\$v\_2\$](img60.png){width="18" height="29"}, **take a screenshot and
verify that ![\$v\_{out}\$](img51.png){width="30" height="29"} is indeed
the difference of ![\$v\_1\$](img59.png){width="18" height="29"} and
![\$v\_2\$](img60.png){width="18" height="29"} with the expected sign.**
