# Anycubic_Kobra_Max
PRUSA Profiles for AnyCubic Kobra Max

# UPDATED Install Method for PRUSA Slicer 2.6.X

PRUSA Slicer has a nasty habit of adding names and stuff when you import an .INI profile. There's a way to get around that and just means you install the profiles from a folder in this archive to the corresponding folder in your PRUSA configuration and don't do a File Import Config..

Download the archive, then run PRUSA Slicer. In PRUSA Slicer Help-->Show COnfiguration Folder

![Configuration_Folder](https://github.com/wabbitguy/Kobra_Max_PRUSA_Profiles/assets/8953419/488c42af-68b2-4b71-ab35-8fc1747299a9)

This will expose the configuration folders PRUSA Slicer uses.

![Folders](https://github.com/wabbitguy/Kobra_Max_PRUSA_Profiles/assets/8953419/2f63e255-92e9-42db-accb-b471b2ed57c0)

QUIT PRUSA SLICER

From the download, copy the CONTENTS of the "filament", "print" and "printer" folders to the folders of the SAME name in the configuration folders. You do not drag and drop folders, you only want the contents of the folders.

Put the KobraMax_Bed.png file in an area you can find on your computer.

Run PRUSA Slicer. You will now have all the profiles for the Kobra Max for various filament types.

If you are using stock firmware, you will probably need to drop the hot end temps in the Filament settings tab because AnyCubic uses the wrong thermistor in their firmware (it runs about 10 - 20C too hot).

The bed SVG is used in "Printer Settings-->General-->Bed Shape-->Texture. Load, ok and then remember to save the profile.

![bed](https://github.com/wabbitguy/Kobra_Max_PRUSA_Profiles/assets/8953419/e5944a6b-9b72-4795-8a27-96951c2d5ef0)

# Old Profile Install

The extrusion mutiplier for these profiles is based on a 100mm feed. My stock Kobra Max had the extrusion eSteps set to 95%. The stock value on my Max was 405. When I calibrated it I ended up with 419.88

You can change the eSteps easily with PRONTERFACE by issuing an M92 E###.## GCODE and then sending an M500 to save the new value in EPROM. To see the stock value use PRONTERFACE and send an M503 GCODE. Then look for the following line:

M92 X80.00 Y80.00 Z400.00 E405.00

If you don't change the eSteps, keep in mind the Extrusion Multiplier could be 5% less.

All profiles created with PRUSA SLICER 2.5.0: https://github.com/prusa3d/PrusaSlicer/releases/tag/version_2.5.0

To use the profiles, select the green "CODE" button --> Download Zip. Save to your hard drive and then unzip.
In PRUSA Slicer: File --> Import --> Import Config and select the config.ini you want.

For the bed:

These are the graphic and STL files for the Chiron Bed that can be used in PRUSA Slicer

To use them move them to are place where they won't get lost or replaced on your hard drive. Run PRUSA Slicer - Printer Settings --> General --> Bed Shape --> Set In the dialog window, Load Texture and select the PNG file Select Load Model and select the STL for the bed.

Note the bed is only partially transparent.


Various brands of filaments were used in testing these profiles. The profile where the temperature is heavily dependant on the brand is TPU. I tested with SainSmart and ERYONE. They print fine at the profile temperature. However with Overture, it needs to be a lot hotter, as in the 218C range.

ABS: PRUSA, kexcelled

PETG: Filaments.ca, ERYONE, Polymaker, GEEETech

PLA: ERYONE, eSun, 3D Solutech, Quantum 3D

TPU: SainSmart, 3D Solutech, ERYONE, Overture (needs higher temp)

HIPS: 3D Printing Canada

The SVG and STL are the custom graphic/model for the bed. Put them in a folder where they own move and then in Printer Settings-->General-->Bed Shape, you can select the two files.

Sept 9 - 2022 - Added DRAFT print profile, created with PRUSA Slicer 2.5.0. Layer height 0.3, fast printing speed, uses volumetric Pressure Equaliizer. To use select the draft prifle, then for the Filament and Printer settings select the filament type you want to use. Hence the DRAFT profile (print settings only) is generic for all filaments. For the higher speed and thicker layer height, you may need to increase the hot end temperature by 5%. Do not recomend draft profile for TPU.

Aug 2023 - With PRUSA Slicer 2.6.0 you don't need the Kobra_Bed.stl file any more.

![Kobra_Bed](https://github.com/wabbitguy/Kobra_Max_PRUSA_Profiles/assets/8953419/caa9498c-5891-4aad-8385-51e7826586dd)
