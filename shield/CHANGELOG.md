# Arduino Shield Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.3.1a] - 2019-06-30
Mostly adjustments after having the first fab run done

### Added
  - N/A

### Changed
  - Silk screens for backlight and OneWire selector moved for visibility
  - Removed some vias and re-routed some traces

### Removed
  - N/A

## [v1.3.1] - 2019-06-02
Update to allow flexible configuration of the backlight.

### Added
  - Jumper cap header to select between backlight on a timer (requires rotary encoder or a button to wake it up) vs having the backlight always on.

### Changed
  - R12 now provides sink for transistor in either backlight configuration.

### Removed
  - Removed R13

## [v1.3] - 2019-06-01
This is v1.3, code named: "The One Shield."  I can't see where we can do anything different with the Arduino Uno.  Perhaps most significantly, this shield provides hardware support for an I2C display (there's important information about this below).  There are other improvements which I think you guys are gonna dig.

If you want to use the I2C there are two important things you need to keep in mind!
1.	I2C support is a separate firmware image and only available in version 0.2.12.  As of right now (6/1/19) this is a beta image, but I should be ready to release it soon.  Firmware 0.2.12 requires BrewPi Scripts/WWW v0.5.2.1 which is currently in the Devel branch.
2.	You MUST select "A0" on the One-Wire selector.

### Added
 - Four-pin I2C header.  No more having to use that 16-pin ribbon!  A mere 4 wires to connect your display. (Yes, the previous parallel LCD is supported as well.)
 - Rotary encoder header - No more having to figure out which Arduino header pins to use!
 - OneWire Selection: One each three-pin header to switch between A0 or A4 for the One-Wire bus.  You must use A0 if you are using I2C.  Not sure why Elco ever used A4 but that's one of the hard-wired I2C pins for the Arduino so a chance was necessary.
 - Break-Out Board support:  An RJ45 to allow for a remote break-out board.  This uses an Ethernet cable (which is straight-through) as opposed to the smaller RJ11 (telephone cord) because phone cords are cross-over by default.  The pin-out supports [USER=221138]@Thorrak[/USER]'s original breakout boards, however support for remotely placing the heat/cool relays is also included.  A breakout board supporting all of this is in development:
   - Pin 1 - Unused
   - Pin 2 - Unused
   - Pin 3 - VCC
   - Pin 4 - OneWire Data (A4 or A0)
   - Pin 5 - GND
   - Pin 6 - Door (D4)
   - Pin 7 - Cool (D5)
   - Pin 8 - Heat (D6)
  - Door pins:  The original Arduino firmware has support for a contact switch which detects when the door is open.  I don't know of many folks using this but adding two pins for that was easy enough since we already put it on the RJ45.
  - Alarm:  The original firmware has VERY basic support for an alarm (piezo speaker).  Right now, it only beeps when the Arduino resets but maybe we can do something more with it later.
  - LCD Backlight always-on:  If one used the v1.2 board with no rotary encoder or at least a switch, the LCD would time-out and not be able to be turned back on.  Added R13 to keep the backlight always-on in those cases.  To make use of this functionality, REMOVE R12 and ADD R13.

### Changed
  - LED headers - The old headers were one pin each for heat and cool, connected to a pull-up resistor.  That worked fine with "normal" setups, but the wiring was not straightforward for what I call "mere mortals." And, if you used non-inverted outputs for heat and cool (such as with SRs) you found yourself in a strange position.  These headers are three-pin: VCC <-> D5/6 <-> GND.  This means if you are using "normal" inverted outputs, you connect your LEDs to VCC and the center pin for either LED.  If you are using non-inverted outputs, you connect the LEDs to GND and the center pin for either LED.
  - Relays: This change re-orders the pins to match the typical relay headers.
  - Power:  Version 1.2 split the power for the LCD and used the ICSP header to power the LCD backlight to reduce LCD scrambling.  By all accounts that had no impact.  On some Arduino clones (as well as the combo ESP8266/ATmega328P boards) have the ICSP header in a different place, which ended up requiring jumpers to apply power to the LCD, and/or creating a shorting point with the pins hitting an unexpected place on the controller board.  This has been re-combined with the power and ground points looped together to form a single larger bus.  In addition, from v0.2.11 of the Arduino firmware, there is a timer which resets the LCD display every 180 seconds to get rid of any scrambling.
  - Parallel LCD header:  Even though the old header was 16-pins, we only used 12 of them.  Using a straight 16 was simpler and kept people form screwing things up too bad but we needed the room.  So, the parallel LCD header is now split into two 6-pin headers.  This does give the benefit of making this connection much easier to route as bending two 6-wire ribbons is a lot easier than a 16-wire one.

### Removed
- N/A

## [v1.2] - 2014-07-10
### Changed
- Replaced mosfet with transistor for easier assembly.

## [v1.1] - 2017-01-27
### Added
- Original version, unknown release date
