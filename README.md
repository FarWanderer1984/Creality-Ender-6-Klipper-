# Creality-Ender-6-Klipper-
My Ender 6 Klipper build

Mainboard Upgraded to BTT Octopus Pro with TMC2209 UART

Extruder and Hot End upgraded to BIQU H2 V2 500 degree

Cr-Touch

Raspberry Pi4 2gig

To-Do

BIQU Hermit Crab Can Bus

Mains Heated Bed


I setup two seperate printer settings for PLA and PETG so the settings and start codes could be tailored for each filiment. this means things line pressure advance, z offset and firmware retraction can be tailered for different filiments and loaded as start of the start_print macro.

PETG machine settings

START_PRINT_PETG

SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET={material_bed_temperature_layer_0}

SET_HEATER_TEMPERATURE HEATER=extruder TARGET={material_print_temperature_layer_0}

PLA machine settings

START_PRINT

SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET={material_bed_temperature_layer_0}

SET_HEATER_TEMPERATURE HEATER=extruder TARGET={material_print_temperature_layer_0}

end code is just End_Print

MY gcode files for my printer to help setup pressure advance, flow rate and z offset.

Pressure advance has the codes added for direct drive so I can just click print and not have to type in the commands for tuning tower. The pressure_advance formula is pressure_advance = <start> + <measured_height> * <factor>. (For example, 0 + 12.90 * .005 would be 0.0645.)

Klipper pressure advance tutorial https://github.com/Klipper3d/klipper/blob/master/docs/Pressure_Advance.md?msclkid=cc98469dae2011ec8f83129ad8d68d2c
  
z_offset is just useed so I can adjust it live and if need be add the SET_GCODE_OFFSET Z=???? to my start print as this way I'm not redoing the offset for each filiment, as PETG can like abit more head room over PLA which can sometimes prefare abit of squish.    
