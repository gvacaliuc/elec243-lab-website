# Experiment 6.1

## Voltage Amplifiers

### Components

* 741 Op Amp
* Resistors as shown on schematics

### Part C: Non-Inverting Amplifier

So far all of the op-amp circuits we have examined have been *inverting*, i.e.
the polarity of the output is inverted with respect to the input. This doesn't
have to be the case, as the following circuit shows:

<center>
![](./figs/img236.png)
</center>

This is an example of the basic *non-inverting* op-amp configuration. A simple
analysis shows that $v_{out}=(1+\frac{R_2}{R_1})v_{in}$ (with no minus sign).
This circuit has a couple of useful characteristics. Most obvious is that it
doesn't invert. Another is that the input impedance is extremely high. One
potential disadvantage is that the minimum value of gain is unity.

1. Using a 741 op amp, wire the non-inverting amplifier circuit. Let $R_1$ be
   1 kΩ. Choose $R_2$ to give a gain of 2.

2. Connect a 1 $V_{pp}$ 1 kHz sine wave to $v_{in}$. Observe $v_{in}$ and
   $v_{out}$ on the oscilloscope.

3. **Take a screenshot. What is the actual gain? Is it in non-inverting?**

### Part D: Difference Amplifier

What if we want the difference, rather than the sum of two signals? We could
combine an inverting amplifier with a summing amplifier to negate one of the
signals before forming a sum, but this would require two op-amps. A simpler
circuit results from combining an inverting and a non-inverting configuration
on the same op-amp, like this:

<center>
![](./figs/img237.png)
</center>

For arbitrary values of the resistors, we get $\displaystyle
v_{out}=-\frac{R_2}{R_1}v_1+\frac{R_4}{R_3+R_4}\frac{R_1+R_2}{R_1}v_2$ which
doesn't seem very useful. However, if we let $R_3=R_1$ and $R_4=R_2$ , then we
have $\displaystyle v_{out}=\frac{R_2}{R_1}(v_2-v_1)$ i.e.  a *difference
amplifier*.

1. Wire the above circuit, using 10 kΩ for all four resistors.

2. Using the function generator for $v_1$ and the 0-6 V power supply for $v_2$,
   **take a screenshot and verify that $v_{out}$ is indeed the difference of
   $v_1$ and $v_2$ with the expected sign.**
