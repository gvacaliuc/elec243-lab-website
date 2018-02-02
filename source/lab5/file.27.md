ELEC 243 Lab

------------------------------------------------------------------------

Prelude
-------

Organizing Your Breadboard
--------------------------

The first four Labs have been something of a "warmup" in terms of
utilizing the breadboard. We've used only one or two of the interface
components at a time and we've built circuits consisting of 2 or 3
components which we've disassembled at the end of lab. With this Lab we
will begin constructing more complicated circuits having more external
connections. Since some of these will perform functions we will need in
other Labs, we will want to leave them in place on the breadboard for
future use. To avoid chaos, we need a plan for organizing the layout and
wiring on the breadboard and interface board.

There are several aspects to this organization ranging from small
details to the big picture.

#### Color Coding

One good practice is to use different colors of wires to denote
different classes of signals. One set of signals you should color code
are power and ground.

In particular, you should have a different color for +15 V, -15 V, and
ground and you should not use any of these colors for other signals. It
would be nice to use "standard" colors for these, but unfortunately
there are several competing standards. One color that nearly everyone
agrees on is that red should be the positive power supply voltage. Most
automotive and electronic wiring uses black to denote ground. Electronic
wiring which uses black for ground often uses blue for the negative
supply. However, our power supply and breadboard use green to denote
ground (the convention used in house wiring) and use black to denote the
negative supply.

So we have two possible "standard" color codes for power: (1)
red = +Vcc, green = gnd, black = -Vcc, and (2) red = +Vcc, black = gnd,
blue  = -Vcc. You could use either of these, or make up your own. The
pictures in this lab use set (1).

Another useful thing to color code would be the wires or "probes" from
the interface board connector. That way you can tell which wire is `CH1`
of the scope or which is the function generator output without having to
trace from one end of the wire to the other.

#### Power Busing

Op amps require external power in order to operate. Since we will be
using several op amps in this and subsequent labs, and each op amp
requires several power connetions, we need an efficient and uncluttered
way of distributing the power supply voltages.

If we plug an [op-amp](../figs/741_photo3.jpg) in with pin 1 in the
lower left corner, then the writing on the package and pins 1 through 4
read left to right. In this case, the positive supply pin is on top and
the negative supply on the bottom. To simplify power wiring, we can run
positive, negative, and ground on each of the triple bus strips. Doing
this and running ground on the remaining buses gives us the following
layout for power:

![\\includegraphics\[scale=0.650000\]{pwr\_bus8.ps}](img231.png){width="595"
height="299"}

We won't need all of these power buses today, but we will in the future,
so we might as well wire them all now.

#### Interface Module Connector Assignments

Some of the connectors on the Interface Modules are dedicated to a
single function (e.g. the telephone handset or the sound card). Others
(e.g. the BNC and phone jacks) are more flexible and may be connected to
a variety of signal sources or destinations. It will be helpful to
establish standard assignments for these connectors as well.

In the instructions and photographs, we will be using the following
assignment:

  ------------------------------------------------------------------------
  **Connector**
  **Socket Pin**
  **Signal**

  J1-1
  1
  Oscilloscope channel 1

  J1-2
  2
  Oscilloscope channel 2

  J1-3
  3
  Function generator output

  J1-4
  4
  Microphone

  J1-7
  10,11
  Handset
  ------------------------------------------------------------------------


