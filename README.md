# Ender 5+ & BTT Octopus
Adventures with an Ender 5 Plus using BigTreeTech Octopus v1.1

### Always exercise extreme caution when doing anything with electricity, especially high voltage!

The information in this repository is licensed under the GPL v3 license unless otherwise already licensed with one that conflicts with this license.

Current Marlin version is 2.0.9.1

Please remember, my printer is most likely different from yours. You may need to make modifications to the configuration and compile your own firmware if you find that mine does not work for you.

The firmware and config contained within the 'works_for_me' branch will always be whatever I'm running successfully on my printer. Other branches may contain newer or older versions that I have not explicitly tested myself.

Below are the changes that I have made to my printer (that I can think of):
* Replaced PSU with Mean Well UHP-500-24 https://www.amazon.com/gp/product/B0796WZBBX
* Replaced stock Ender controller with BTT Octopus
* Replaced stock display with BTT TFT50 v3.0
* Replaced X,Y motion with ExoSlide https://www.exoslide.com/products/kits/ender5plus-XY
* Replaced bed springs with silicone mounts https://www.amazon.com/gp/product/B07S2R5C6P

The firmware is configured for independent Z axis control. Since this printer already has separate steppers for each of the two Z lead screws it only makes sense to enable G34 capabilities.

Not much remains of the original Ender 5+ kit. I also use OctoPrint on a Raspberry Pi4 to manage print files. I do not print directly from the Octopus controller.

If you have problems or issues I recommend Google and the Marlin Discord channel.

## Firmware settings/tuning:

### Steps/mm
* X 80 
* Y 80
* Z 800
* E 100

### Feedrate mm/s
* X 8000
* Y 8000
* Z 15
* E 15000

### Acceleration mm/s2
#### Printing
* Printing 500
* Retract 1000
* Travel 1000
#### Maximum
* X 5000
* Y 5000
* Z 100
* E 10000

### Offsets
#### Home
* X 0mm
* Y 0mm
* Z 0mm
#### Probe
* Z probe X offset -46mm
* Z probe Y offset -5mm
* Z probe Z offset -1.8mm

### PID
#### Hotend PID
* kP 26.8234
* kI 2.3949
* kD 75.1056

### TMC Driver Current
* E0 Stepper 800mA
* X Stepper 800mA
* Y Stepper 800mA
* Z Stepper 800mA

### Linear Advance
* K factor 1.41

### Advanced
* Minimum segment time 20000
* Junction Deviation 0.08
* Minimum feedrate for print moves 0mm/s
* Minimum feedrate for travel moves 0mm/s
