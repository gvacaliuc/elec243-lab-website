# Tips for Using Spice

Here is a collection of pointers and instructions to refer to when using Spice.
This should be enough to get you started, but you can also refer to this [user
manual](http://www.eecg.toronto.edu/~kphang/teaching/spice/).

* Place components by going to the Edit menu or shortcut buttons.

* The opamp is found under Edit $\rightarrow$ Components $\rightarrow$ OpAmps
  $\rightarrow$ opamp. The voltage source is found under Edit $\rightarrow$
  Components $\rightarrow$ voltage. Connect components using Edit
  $\rightarrow$ Wire (or the shortcut button F3).

* Set the voltage source  to AC by right-clicking it and selecting Advanced.
  Set AC amplitude to 1.

* Enter in R and C values by right-clicking these components.  

* Optional label nets (i.e., wires) by right-clicking on nets.  

### Keyboard Shortcuts

|  **Shortcut**   | **Description** |
|  ------------   | --------------- |
|     Ctrl-R      |      Rotate     |
|   Delete or F5  |      Delete     |
|        F6       |       Copy      |
|        F7       |       Move      |
|        F8       |       Drag      |
|        Esc      |   Exit a mode   |

### Performing an AC Analysis

1. Click on the Running Man icon and select AC analysis (or go to Simulate
   $\rightarrow$ Run).

2. Use a decade frequency sweep with at least 10 points per decade over the
   range of 1 Hz to 10 MHz. This will appear as a Spice directive on your
   schematic as `.ac dec 10 1 10meg`

3. Click on the `Vout` node for gain and phase plots to appear. You will
   notice that the gain is displayed in dB and phase in degrees. The x-axis
   will be logarithmic, i.e., the step size is $10^n$, where $n \in
   \mathbb{Z}_+$.  Each of the steps is called a decade (dec).
