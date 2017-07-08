Please see docs/pcbgcode.pdf.


# pcb-gcode
This is a modified and bug-fixed version of the super nice Eagle plugin to generate gcode directly out of Eagle to be used on general purpose PCB mills based on grbl or reprap machines.

# New, additional features
* This version allows you to define sliced for PCB outline milling. Originall, the code only ran the path once which resulted in broken bits or bad, slow milling - which then results in worn out bits due to overheating.
* Bug fixed that caused the etch bit (usually a V-shaped engraving bit) to spot drill all the way to drill depth instead of spot drill depth. This widens holes significantly and wears out your engraving bit! That bug is now gone and needs testing. See file pcb-file-utils.h at the bottom for details. I have no idea, yet, why the first whole is different from all the other holes. Makes no difference in the gCode for me.

# Usage
* Load the Design rule file that I also provided: 20170624 - Eagle Design Rules NuggetMill5.dru
* Start the program by typing: 
```
run pcb-gcode-setup
```
* or, if you have configured everything already
```
run pcb-gcode
```