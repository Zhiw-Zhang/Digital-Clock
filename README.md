# MCU-Based Digital Clock Design

Chinese version: [README.zh-CN.md](README.zh-CN.md)

## Development Platform
- MCU: Texas Instruments (TI) MSPM0L1306 development board
- Development environment: Keil with SysConfig graphical configuration tool

## Main Features
1. **1-second timing**: Uses timer interrupts to achieve precise 1s timing, and drives an LED to blink once per second through an IO pin.
2. **24-hour clock**: Displays current hour, minute, and second on the OLED with correct time progression and carry.
3. **Calendar**: Displays date information (year, month, day, and weekday) on the OLED.
4. **Time and date setting**: Supports setting the current time and date via matrix keypad.
5. **12-hour mode**: Displays AM/PM in 12-hour mode and supports switching between 12/24-hour formats via keypad.
6. **Alarm**: Supports 3 independent alarms with configurable time and on/off state.
7. **Timer**: Displays elapsed time in seconds, and supports start, pause, stop, and reset operations via keypad.

## Key Mapping
From left to right, top to bottom, the keys are mapped as:
`1,2,3,u,4,5,6,d,7,8,9,l,q,0,y,r`

You can also check the `keyboard` function in [main.c](Core/src/main.c).

>[!tip]
>1. This project was built from an empty project template. The main self-written parts are [main.c](Core/src/main.c) and [DIGITAL_CLOCK.syscfg](DIGITAL_CLOCK.syscfg) (configured via SysConfig).
>2. The alarm setting flow may show garbled characters during configuration, but it does not affect the actual setting result.
>3. The timer function may occasionally show garbled characters; resetting and restarting the timer fixes it.
>4. This was an early development project, and all code is placed in [main.c](Core/src/main.c), so readability is not ideal.
