### Klipper Config

* Ender 3 V2
* 4.2.7 Mainboard
* E3D Hemera / V6 Hotend
* Hemera Mount: https://www.thingiverse.com/thing:4785386
* BLTouch Antclabs v3.1


### PID Tune

TURN_OFF_HEATERS  
PID_CALIBRATE HEATER=extruder TARGET=235

TURN_OFF_HEATERS  
PID_CALIBRATE HEATER=heater_bed TARGET=60

### Probe Z Offset

G28  
PROBE_CALIBRATE  
TESTZ z=-5 / TESTZ z=- / TESTZ z=+  
SAVE_CONFIG

### Bed Mesh

BED_MESH_CALIBRATE  
SAVE_CONFIG


### Hemera Rotation Distance (E-Steps Calculation)

```
rotation_distance = <full_steps_per_rotation> * <microsteps> / <steps_per_mm>
```

```
((360 / 1.8) * 16) / 409 = 7.82
```

### Calculate pressure_advance
### Calculate input_shaping
