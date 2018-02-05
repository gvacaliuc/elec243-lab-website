ELEC 243 Lab

------------------------------------------------------------------------

Introduction
============

Voltages in a circuit (so called analog signals) are continuous whereas
the sequence of numbers in the computer with which we are representing
it is discrete, both in time and in value. In other words, by sampling
the analog signal at regular intervals we ignore any changes that may
take place between these sampling times, and by representing the value
by a number with a limited number of digits we introduce an error
between the actual value and its representation. In the first part of
this lab we will observe sampling effects using Labview.

Next, we will look at how we might use the computer alongside (or
instead of) op amps as part of an overall signal processing system. We
will look at some processing functions (e.g. filtering) which are direct
"analogs" of analog processing, as well as some that would be difficult
or impossible to implement in an analog circuit. For this, we will use
Matlab to do most of our signal processing.

Matlab has a more conventional programming language, and it allows us to
circumvent the real time constraint by using "batch" processing: we
record a signal on disk, process it (taking as long as we need), write
the resulting output to disk, and then play back the output signal. This
has the additional advantage of allowing us to perform different
processing functions on exactly the same input (reference) signal and
compare the results.

We will also look a bit further into the process of filter design and
implementation. Then we will try generating signals digitally, as well
as filtering them. Finally, we'll look at some applications that are
more elaborate than simply filtering signals.
