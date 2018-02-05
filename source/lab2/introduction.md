# Introduction

The terms DC (short for Direct Current) and AC (Alternating Current)
originated in the early days of electric power to differentiate the
system developed by Thomas Edison from that invented by Nicola Tesla and
supported by George Westinghouse. In Edison's system the current flowed
continuously in one direction, while the direction of Tesla's current
alternated at a frequency of 60 Hz. Today the terms are used somewhat
more loosely, with DC referring to signals which are constant or only
slowly time varying, while AC can mean any rapidly changing signal.

Strictly speaking an AC signal should be *bipolar,* i.e. having a sign
which alternates with time. While it's certainly possible to have a
time-varying signal whose sign never changes, it's not possible to have
one which is strictly monotonic. I.e. what goes up must come down, even
if it never hits the ground. In this case we sometimes refer to the DC
and AC *components* of a signal, more precisely defined as the average
value and the variations about that average.

An important class of time-varying signals are *periodic* signals for which
$f(t) = f(t + nT)$ where $T$ is the *period* of the signal, and n is an
integer. We can completely characterize a periodic signal by describing its
*waveshape* (e.g. a sinusoid), its *amplitude*, and its *frequency*.

The signals we measured last week were DC signals and could be described
by a single number. This week we will look at a variety of AC signals
which, in addition to being more interesting, can contain a greater
amount of information.
