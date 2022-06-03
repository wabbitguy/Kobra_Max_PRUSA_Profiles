# Anycubic_Kobra_Max
PRUSA Profiles for AnyCubic Kobra Max

The extrusion mutiplier for these profiles is based on a 100mm feed. My stock Kobra Max had the extrusion eSteps set to 95%. The stock value on my Max was 405. When I calibrated it I ended up with 419.88

You can change the eSteps easily with PRONTERFACE by issuing an M92 E###.## GCODE and then sending an M500 to save the new value in EPROM. To see the stock value use PRONTERFACE and send an M503 GCODE. Then look for the following line:

M92 X80.00 Y80.00 Z400.00 E405.00

If you don't change the eSteps, keep in mind the Extrusion Multiplier could be 5% less.

Various brands of filaments were used in testing these profiles. The profile where the temperature is heavily dependant on the brand is TPU. I tested with SainSmart and ERYONE. They print fine at the profile temperature. However with Overture, it needs to be a lot hotter, as in the 218C range.

PETG: Filaments.ca, ERYONE, Polymaker, GEEETech

PLA: ERYONE, eSun, 3D Solutech, Quantum 3D

TPU: SainSmart, 3D Solutech, ERYONE, Overture (needs higher temp)

HIPS: 3D Printing Canada
