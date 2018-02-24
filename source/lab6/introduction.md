ELEC 243 Lab

------------------------------------------------------------------------

Introduction
============

Last week we looked at several op-amp circuits for amplifying voltages.
While there are many things you can do with a voltage amplifier, there
are also many things that you can't. In particular, the optoelectronic
transducers we studied in Lab 2 have nonlinear behavior in terms of
their voltages, but very linear behavior in terms of current. To
effectively utilize these, we will need amplifiers which accept and
deliver currents rather than voltages.

Some of our other transducers are resistive: they produce neither
voltages nor currents on their own, but must be used in conjunction with
voltage or current sources to produce a usable signal. For transducers
which produce large changes in resistance in response to the physical
quantity being measured, the circuits we used in Labs 3 and 4 are
satisfactory. However some transducers, such as strain gauges, produce
only very small changes in resistance. For satisfactory results with
these, we will need a new circuit: the *bridge*.
