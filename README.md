# YAGT
Yet Another Guitar Tuner
A simplistic clip-on tuner using 3 LEDs as tuning status:
  Note: RGB LED 
  Too High Red led
  Too Low: Red led
  
  These LEDS can be incorporated into a tuning 'head' with High/Low as the eyes and Note as the Nose or mouth.
  
Theory of Operation:
A piezo contact probe is amplified by a jfet/opamp stage followed by a Sallen-Key anti-alias filter.
The resultant signal is digitized by the 12 bit ATD input of an STM32L031. 
Each captured frame of audio is analyzed using autocorrelation and interpolation of the peak to define the note frequency.
A watch crystal provides the frequency reference for the analysis.

A demonstration clip is provided as OpenScad files which may be exported and 3d Printed.
The tuner is switched on by two wipers contacting a ring in the clip base when rotated off the dead zone.
The battery used is a 1/2 AA lithium type.

Included: 
- Firmware
- Schematic
- KiCad layout
- OpenScad clip files with demo head
