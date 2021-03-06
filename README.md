# Eleksmaker A3 Pro

I run my eleksmaker under ubuntu. No additional drivers where needed to communicate with the arduino nano clone.
Never tried out the original firmware so I have no clue how this would have worked.
I'm pretty happy with Laserweb and Grbl.

## Software
- [Grbl 1.1](https://github.com/gnea/grbl)
- [Laserweb 4](https://github.com/LaserWeb/LaserWeb4)

## Setup
0. Make sure to always wear Eye protection when working with the laser. It sometimes turns on the laser when you connect to it.
1. Get arduino ide, clone grbl 1.1 and flash grbl. The firmware does not need to be changed.
2. Get Laserweb 4 and connect to your laser.
3. Once connected change the settings via the built-in terminal (you find my settings below)

## Grbl Settings

```
$0=10      ;Step pulse, microseconds
$1=25      ;Step idle delay, milliseconds
$3=1       ;X axis direction inverted
$10=0      ;send work coordinates in statusReport
$30=255    ;max. S-value for Laser-PWM (is referenced to the LaserWeb PWM MAX S VALUE)
$31=0      ;min. S-value
$32=1      ;Laser Mode on
$100=80   ;steps/mm in X, depending on your pulleys and microsteps
$101=80   ;steps/mm in Y, depending on your pulleys and microsteps
$102=80   ;steps/mm in Z, depending on your pulleys and microsteps
$110=10000 ;max. rate mm/min in X, depending on your system
$111=10000 ;max. rate mm/min in Y, depending on your system
$112=10000 ;max. rate mm/min in Z, depending on your system
$120=1000  ;acceleration mm/s^2 in X, depending on your system
$121=1000  ;acceleration mm/s^2 in Y, depending on your system
$122=300   ;acceleration mm/s^2 in Z, depending on your system
$130=400   ;max. travel mm in X, depending on your system
$131=300   ;max. travel mm in Y, depending on your system
$132=100   ;max. travel mm in Z, depending on your system
$$         ;to check the actual settings
```

These settings are based on [this wiki page](http://itink.it/wiki/doku.php?id=en:tinkering:laser:eleksmakera3pro).
Note: I had to change the steps/mm of all axis to `80` instead of `160`

## Tutorials
- Setup explained: https://www.youtube.com/watch?v=psnbSPrdy0I

## Materials

### Wood (Engraving)

Tested with different kinds of wood (Plywood, birch, spruce)

- Speed / Cut Rate: 1200 mm/m
- Passes: 1
- Power: 100%

### Wood (Cutting)

#### Plywood 4mm

- Speed / Cut Rate: 300 mm/m
- Passes: 35
- Power: 100%
