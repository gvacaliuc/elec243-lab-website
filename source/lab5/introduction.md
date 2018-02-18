# Introduction

Now that we are experts on Labview, able to process and display any signal we
can digitize, we need to become experts on what happens in the analog world
between the transducer and the A/D converter. The process of effectively and
efficiently connecting a transducer to the remainder of the measurement system
is often referred to as *signal conditioning*.  Some of the conditions which
need to be met before delivering a signal to the A/D converter include:

**It must be a voltage.**

The A/D converter only converts voltages. If we have a current, resistance, or
other type of signal, it must be converted to a voltage before being digitized.
We did this last week with the thermistor and photocell, which respond to
physical variables by changes in resistance.

**It should efficiently utilize the range of the A/D converter.**

The range of A/D channels 0-3 is $\pm 100 V$ and that of channels 4-7 is $\pm
10 V$. All of the signals we have seen so far fit comfortably in one or both of
these ranges. However, the A/D conversion process is *quantized*. The resulting
digital value is represented as a 16-bit integer. This means that the
*resolution* of a digitized measurement is $\frac{1}{2^{16}}$ of the total
range, i.e. the $200 V$ or $20 V$ range is divided into steps of $3.1 mV$ or
$0.31 mV$.  Any input or change in input smaller than this will go unnoticed.

**It must have an appropriately limited bandwidth.**

In Experiment 3.1 we saw that funny things can happen if the frequency of a
signal is higher than the rate at which we sample the signal. In fact, bad
things happen if any component of the signal being digitized has a frequency
greater than *half* the sampling rate.

**It should contain a minimum amount of noise.**

It's always better to eliminate noise at the source than to try to reduce its
effect after it is already in the system.

Meeting these conditions will be the goal of the next group of labs. We will
begin this week with a look at the *operational amplifier*, or *op-amp* for
short. In addition to simply amplifying signals, this versatile component can
perform or assist in all of the other tasks in our signal conditioning list.
However, since amplifying is (at least conceptually) simple, we'll start by
looking at amplifiers.

An amplifier is characterized by its *gain*, the ratio of its output to its
input. If the input and output are both voltages (the most common case) the
gain is $A=\frac{v_{out}}{v_{in}}$.  $A$ can be either positive or negative.
If it is negative we say that we have an *inverting* amplifier.

If we want to make a point that the gain is a ratio of voltages we can call it
*voltage gain* and write it as $A_v$.  This is because there are other
quantities besides voltage that we can amplify.  For example, we could have a
*current amplifier* where $i_{out} = A_i i_{in}$, with $A_i$ being the
*current gain*.
