ELEC 243 Lab

------------------------------------------------------------------------

Experiment 2.1
--------------

Measuring Heat and Light
------------------------

### Equipment

-   [BNC clip leads](figs/clip_leads.jpg)
-   [BNC-banana adapter](figs/banana_adapter.jpg)

### Components

-   [10K Thermistor](https://media.digikey.com/pdf/Data%20Sheets/Panasonic%20Sensors%20PDFs/ERTD_Series.pdf)
-   [CdS
    Photocell](https://media.digikey.com/pdf/Data%20Sheets/Photonic%20Detetectors%20Inc%20PDFs/PDV-P9001.pdf)
-   [Photodiode](http://www.ttelectronics.com/sites/default/files/download-files/OP905-906_1.pdf)

### Part 1: Thermistor

In Part 4 of Experiment 1.1 we found that the resistance of the light
bulb filament increased with increasing temperature. Materials (such as
metals) which exhibit this behavior are said to have a *positive
temperature coefficient*. Materials (such as semiconductors) whose
resistance decreases with temperature have a *negative temperature
coefficient* (NTC). The thermistor is a piece of NTC material whose
resistance is described by the equation ![\$R=R\_0
e\^{B(\\frac{1}{T}-\\frac{1}{T\_0})}\$](img20.png){width="122"
height="43"} , where ![\$R\$](img9.png){width="15" height="14"} is the
resistance at the measured temperature ![\$T\$](img21.png){width="15"
height="14"} and ![\$R\_0\$](img10.png){width="22" height="30"} is the
resistance at the reference temperature
![\$T\_0\$](img22.png){width="19" height="30"}. Note that the
temperatures must be absolute temperatures (in K).

+--------------------------+--------------------------+--------------------------+
|                          |                          | \                        |
+--------------------------+--------------------------+--------------------------+
| #### Step 1:             |                          | In this experiment we    |
|                          |                          | will need to make        |
|                          |                          | resistance measurements  |
|                          |                          | in situations where      |
|                          |                          | using the DMM probes or  |
|                          |                          | banana plug patch cords  |
|                          |                          | will not be              |
|                          |                          | satisfactory.            |
|                          |                          | Fortunately, there is a  |
|                          |                          | very convenient way to   |
|                          |                          | do this. Get a BNC clip  |
|                          |                          | lead cable from the      |
|                          |                          | equipment room and       |
|                          |                          | attach it to the         |
|                          |                          | BNC-banana adapter from  |
|                          |                          | your tool kit, thereby   |
|                          |                          | creating a *banana plug  |
|                          |                          | clip lead cable*. Plug   |
|                          |                          | the banana plug end of   |
|                          |                          | this assembly into the   |
|                          |                          | `V` and `COM` terminals  |
|                          |                          | of your DMM and set the  |
|                          |                          | selector switch to Ω.\   |
|                          |                          | \                        |
+--------------------------+--------------------------+--------------------------+
| #### Step 2:             |                          | Connect the clip leads   |
|                          |                          | to the terminals of the  |
|                          |                          | thermistor.\             |
|                          |                          | \                        |
+--------------------------+--------------------------+--------------------------+
| #### Step 3:             |                          | Wait until the           |
|                          |                          | resistance reading on    |
|                          |                          | the DMM has stabilized,  |
|                          |                          | and record this value R\_0.    |
|                          |                          | This is  the resistance at     |
|                          |                          | ambient room             |
|                          |                          | temperature T\_0.\            |
|                          |                          | \                        |
+--------------------------+--------------------------+--------------------------+
| #### Step 4:             |                          | Place the thermistor in  |
|                          |                          | contact with your body.  |
|                          |                          | When the resistance      |
|                          |                          | reading has stabilized,  |
|                          |                          | record the value R.\       |
|                          |                          | \                        |
+--------------------------+--------------------------+--------------------------+
| #### Question 5:         |                          | Estimate the ambient temperature in the room. Using your measurements and B value (see [thermistor datasheet](https://media.digikey.com/pdf/Data%20Sheets/Panasonic%20Sensors%20PDFs/ERTD_Series.pdf)), what is your body temperature?             |
+--------------------------+--------------------------+--------------------------+

### Part 2: CdS Photocell

Also known as a photoconductive cell or photoresistor, this device
changes its resistance as a function of incident illumination. One
useful characteristic of cadmium sulphide is that its spectral response
closely matches that of the human eye. That means that a CdS photocell
can be used in some photographic and photometric applications without
additional filtering.

+--------------------------+--------------------------+--------------------------+
|                          |                          |                          |
+--------------------------+--------------------------+--------------------------+
| #### Step 1:             |                          | Remove the thermistor    |
|                          |                          | from the clip leads and  |
|                          |                          | replace it with the CdS  |
|                          |                          | photocell.               |
+--------------------------+--------------------------+--------------------------+
| #### Step 2:             |                          | Note the change of       |
|                          |                          | resistance as the        |
|                          |                          | illumination of the      |
|                          |                          | photocell changes.       |
|                          |                          | Record a few interesting |
|                          |                          | values (e.g. ambient,    |
|                          |                          | illuminated by           |
|                          |                          | incandescent lamp,       |
|                          |                          | covered with hand,       |
|                          |                          | etc.).                   |
+--------------------------+--------------------------+--------------------------+
| #### Question 6:         |                          | Based on the nominal     |
|                          |                          | characteristics of the   |
|                          |                          | photocell, what is the   |
|                          |                          | ambient illumination     |
|                          |                          | level in the lab? What   |
|                          |                          | is the illumination      |
|                          |                          | level at a distance of   |
|                          |                          | one foot from the        |
|                          |                          | incandescant lamp?       |
+--------------------------+--------------------------+--------------------------+
| #### Step 3:             |                          | Measure the dark         |
|                          |                          | resistance of the        |
|                          |                          | photocell. How long does |
|                          |                          | it take for the measured |
|                          |                          | value to stabilize?      |
+--------------------------+--------------------------+--------------------------+

### Part 3: The Photodiode

The thermistor and photocell are *passive* transducers: in order to
convert the changes in resistance into an electrical signal an external
source of electrical power is required. There is another class of
sensors, called *self-generating*, which convert the applied input
directly to an electrical signal. One such transducer is the
*photodiode* which converts incident optical power into electrical
power.

+--------------------------+--------------------------+--------------------------+
|                          |                          |                          |
+--------------------------+--------------------------+--------------------------+
| #### Step 1:             |                          | Remove the CdS photocell |
|                          |                          | from the clip leads and  |
|                          |                          | replace it with the      |
|                          |                          | photodiode.              |
+--------------------------+--------------------------+--------------------------+
| #### Step 2:             |                          | Set the DMM selector to  |
|                          |                          | DC Volts.                |
+--------------------------+--------------------------+--------------------------+
| #### Step 3:             |                          | Observe the changes in   |
|                          |                          | voltage produced by the  |
|                          |                          | photodiode as the amount |
|                          |                          | of light reaching it is  |
|                          |                          | changed. Record the      |
|                          |                          | voltages for the same    |
|                          |                          | conditions you did for   |
|                          |                          | the CdS photocell in     |
|                          |                          | Part 2.                  |
+--------------------------+--------------------------+--------------------------+
| #### Step 4:             |                          | Examination of the data  |
|                          |                          | sheet for the photodiode |
|                          |                          | shows that it is the     |
|                          |                          | *current* rather than    |
|                          |                          | the *voltage* which is   |
|                          |                          | proportional to the      |
|                          |                          | incident illumination.   |
|                          |                          | Set the DMM to DC        |
|                          |                          | Current and connect the  |
|                          |                          | clip leads to the `COM`  |
|                          |                          | and `300 mA` terminals.  |
|                          |                          | (Since the spacing       |
|                          |                          | between these two        |
|                          |                          | terminals is not the     |
|                          |                          | same as the spacing      |
|                          |                          | between the plugs on the |
|                          |                          | banana plug adapter, you |
|                          |                          | will have to insert one  |
|                          |                          | plug into one of the     |
|                          |                          | terminals and use a      |
|                          |                          | banana plug patch cord   |
|                          |                          | to connect the other.)   |
+--------------------------+--------------------------+--------------------------+
| #### Step 5:             |                          | Observe the changes in   |
|                          |                          | the current produced by  |
|                          |                          | the photodiode as the    |
|                          |                          | amount of light reaching |
|                          |                          | it is changed. Record    |
|                          |                          | the current values for   |
|                          |                          | the same conditions you  |
|                          |                          | did previously in Part 2 |
|                          |                          | and Step 3.              |
+--------------------------+--------------------------+--------------------------+
| #### Question 7:         |                          | Based on the nominal     |
|                          |                          | characteristics of the   |
|                          |                          | photodiode, what is the  |
|                          |                          | ambient illumination     |
|                          |                          | level in the lab? What   |
|                          |                          | is the illumination      |
|                          |                          | level at a distance of   |
|                          |                          | one foot from the        |
|                          |                          | incandescant lamp? How   |
|                          |                          | do these values compare  |
|                          |                          | with those measured with |
|                          |                          | the CdS photocell?       |
+--------------------------+--------------------------+--------------------------+


