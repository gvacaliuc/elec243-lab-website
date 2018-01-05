ELEC 243 Lab

------------------------------------------------------------------------

Experiment 2.2
--------------

Electroacoustic Transducers
---------------------------

### Components

-   Loudspeaker
-   Microphone

  ------------------------ ------------------------ ------------------------
                                                    
  ------------------------ ------------------------ ------------------------

### Part 1: Listening to a Signal

+--------------------------+--------------------------+--------------------------+
|                          |                          |                          |
+--------------------------+--------------------------+--------------------------+
| #### Step 1:             |                          | Set up the function      |
|                          |                          | generator to produce a   |
|                          |                          | 1kHz sine wave with a    |
|                          |                          | peak to peak (p-p)       |
|                          |                          | amplitude of 5 volts.    |
+--------------------------+--------------------------+--------------------------+
| #### Step 2:             |                          | Using the [BNC clip      |
|                          |                          | leads](figs/clip_leads.j |
|                          |                          | pg),                     |
|                          |                          | connect the output of    |
|                          |                          | the function generator   |
|                          |                          | to the speaker. What do  |
|                          |                          | you hear?                |
+--------------------------+--------------------------+--------------------------+
| #### Step 3:             |                          | With the speaker still   |
|                          |                          | connected to the         |
|                          |                          | function generator,      |
|                          |                          | measure the amplitude of |
|                          |                          | the voltage across the   |
|                          |                          | speaker (use a second    |
|                          |                          | BNC clip lead). Is it    |
|                          |                          | the same as in Step 1?   |
+--------------------------+--------------------------+--------------------------+
| #### Step 4:             |                          | Using the controls on    |
|                          |                          | the function generator,  |
|                          |                          | vary the amplitude,      |
|                          |                          | frequency, and waveshape |
|                          |                          | (i.e. sine, triangle, or |
|                          |                          | square) of the signal.   |
|                          |                          | How does the nature of   |
|                          |                          | the sound change as      |
|                          |                          | these signal parameters  |
|                          |                          | change?                  |
+--------------------------+--------------------------+--------------------------+
| #### Step 5:             |                          | Disconnect the speaker.  |
+--------------------------+--------------------------+--------------------------+

### Source Loading

If we consider the following circuit:

![\\includegraphics\[scale=0.650000\]{../241/fig4.ps}](img221.png){width="338"
height="175"}

we can see what caused the reduction in signal amplitude (attenuation):
![\$R\_{out}\$](img27.png){width="35" height="30"} of the function
generator and ![\$R\_L\$](img28.png){width="25" height="30"} of the
speaker form a voltage divider. An ideal voltage source would have
![\$R\_{out}=0\$](img29.png){width="64" height="30"} and there would be
no problem. However, any real source will have non-zero
![\$R\_{out}\$](img27.png){width="35" height="30"} . To reduce the
attenuation caused by loading, we can either reduce
![\$R\_{out}\$](img27.png){width="35" height="30"} or increase
![\$R\_L\$](img28.png){width="25" height="30"} . But, since
![\$R\_{out}\$](img27.png){width="35" height="30"} and
![\$R\_L\$](img28.png){width="25" height="30"} are actually parts of the
source and load respectively, that means we would have to replace either
the source or the load with a "better" one. If this is not feasible, we
can isolate the source from the load by placing an *amplifier* between
them.

### Part 2: Viewing an Acoustic Signal

The physical phenomenon behind the operation of the loudspeaker works in
both directions: in addition to converting an electrical signal into an
acoustical signal it can also convert sound to electricity. In techspeak
we say that the loudspeaker is a *bilateral* transducer.

+--------------------------+--------------------------+--------------------------+
|                          |                          |                          |
+--------------------------+--------------------------+--------------------------+
| #### Step 1:             |                          | Using the BNC clip       |
|                          |                          | leads, connect the       |
|                          |                          | speaker to `CH1` of the  |
|                          |                          | oscilloscope.            |
+--------------------------+--------------------------+--------------------------+
| #### Step 2:             |                          | Set the `VOLTS/DIV`      |
|                          |                          | switch to `20 mV` and    |
|                          |                          | the `TIME/DIV` switch to |
|                          |                          | `2 mSEC`.                |
+--------------------------+--------------------------+--------------------------+
| #### Step 3:             |                          | Speak into the           |
|                          |                          | loudspeaker and observe  |
|                          |                          | the waveform on the      |
|                          |                          | oscilloscope. If         |
|                          |                          | necessary, adjust the    |
|                          |                          | oscilloscope to produce  |
|                          |                          | a satisfactory trace.    |
|                          |                          | Note the amplitude of    |
|                          |                          | the signal.              |
+--------------------------+--------------------------+--------------------------+

### Part 3: Microphone

Although we can use the loudspeaker as both an electricity to sound
transducer and a sound to electricity transducer, the fact that its
construction has been optimized for producing sound rather than
accepting sound means that its performance is suboptimal for the latter
task. When we reoptimize for conversion of acoustic to electrical
signals, we get a device called a *dynamic microphone*.

#### Step 1:

Get a microphone from the supply room. It has two connectors, one
slightly smaller than the other. We will use the larger one.

![](figs/mic_conns.jpg)

(The small one is connected to the switch to turn a cassette recorder on
and off when dictating).

We want to use the scope to measure the microphone's output, but
attempting to connect the clip leads to the microphone connector is an
exercise in futility. So ...

#### Step 2:

Use a BNC patch cord to connect `CH1` of the scope to J1-1 of the
[interface module](unilab/interface.html#interface_picture).

#### Step 3:

Plug the microphone into J1-4 of the interface module. Take a piece of
wire about 4 cm long and strip 6 to 7 mm of insulation from each end.
The end of the wire should look like this:

![](figs/stripped.jpg)

  ------------------------------------------------------------------------
  **Note**
  The stripped length of a wire is very important. If it is too short
  (less than 6 mm), insulation will be forced between the contact fingers
  of the socket strip, resulting in an intermittent connection (or none at
  all). This is the second most common cause of problems in the lab. If it
  is too long, the bare portion of the wire above the socket strip can
  short to other wires.
  ------------------------------------------------------------------------

Connect the microphone to Channel 1 of the scope by plugging one end of
the wire into pin 1 of the [socket
strip](../unilab/interface.html#interface_socket) and the other end into
pin 4. The grounds are connected automatically by the interface board.

![](figs/photo2.2.1a1.jpg)

#### Step 4:

Set the oscilloscope `V MODE` switch to `CH1`, the `CH 1 VOLTS/DIV`
switch to `5 mV`, and the `TIME/DIV` switch to `1 mSEC`. Set the other
controls as required.

#### Step 5:

Speak, sing, or whistle into the microphone and observe the signal on
the scope. If the amplitude is too small, you can use the *magnifier* to
get a little more gain.

#### Step 6:

Produce a sustained vowel (a, e, i, o, u) sound. Sketch one or two of
the more interesting waveshapes.

#### Step 7:

Continue producing a sustained vowel sound (inhaling as necessary) and
measure its frequency (by measuring the period).

#### Step 8:

(Optional) If you are musically inclined, sing (or whistle or hum) the
note "A" and measure its frequency. How does your measured frequency
compare with the "official" value for the frequency of A? Which do you
trust to be more accurate, your sense of pitch or the oscilloscope?

#### Step 9:

Whistle softly into the microphone. (For this step, pitch is not
important, so any note will do.) Observe the waveform on the
oscilloscope. Is it sinusoidal?

Based on your measurements of the loudspeaker sensitivity and the output
of the microphone, would it be possible to produce an audible sound in
the loudspeaker by connecting it directly to the microphone?
