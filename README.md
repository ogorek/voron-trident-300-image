# voron-trident-300-image
Voron Trident 300 Raspberry Pi image

Optimised for this configuration
raspberry 4
Voron 300x300
LDO kit
Phaetus Rapido HF
BTT SFS version 2.0
Beacon
BTT Octopus 1.0/1.1


Download always actual link from

https://drive.google.com/file/d/1dkrawz9RilvsQMc3R8sTi7SP6nbCeiaG/view?usp=sharing

Write to sd card with balenaetcher version 1.18.4, version 1.19+ may produce errors codes before writing.
By default, will try to connect to wifi ssid adam password raspberry
No wifi = ethernet dhcp
You can also connect to wifi from voron touch screen
SSH login user adam password raspberry

default interface http://voron.local/ if You prefer fluidd http://voron.local:81 

BTT SFS v2 connect to default ports on octopus like in manual.
Attached mounting plate for sfs v2 3mf format.
When done with testing, switch 2 lines in SFS.cfg from False to True to enable automatic pause when runout is detected.

Update apps, delete, add features like octoeverywhre using this command
/home/adam/kiauh/kiauh.sh

in orcaslicer add to machine start g-code SFS=1 or SFS=0 to choose if to use sensor on first layer
should look like this
M190 S[bed_temperature_initial_layer_single]
M109 S[nozzle_temperature_initial_layer]
PRINT_START EXTRUDER=[nozzle_temperature_initial_layer] BED=[bed_temperature_initial_layer_single] SFS=0

also in layer change g-code need to add this
;AFTER_LAYER_CHANGE
new_layer NUM={layer_num}
;[layer_z]

