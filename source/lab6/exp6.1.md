ELEC 243 Lab

------------------------------------------------------------------------

Experiment 6.1
--------------

Voltage Amplifiers
------------------

### Components

-   741 Op Amp
-   Resistors as shown on schematics

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

- Using a 741 op amp, wire the non-inverting amplifier circuit. Let
![\$R\_1\$](img52.png){width="22" height="30"} be 1 kΩ. Choose
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
