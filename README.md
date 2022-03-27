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

START_PRINT_PLA

SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET={material_bed_temperature_layer_0}

SET_HEATER_TEMPERATURE HEATER=extruder TARGET={material_print_temperature_layer_0}

end code is just End_Print
