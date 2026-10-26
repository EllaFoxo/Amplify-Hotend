![Amplify Render](Assets/cover_480p.png)

# Amplify Hotend

![Amplify Logo](Assets/amplify.svg)

A hotend with an integrated load cell, for nozzle probing, and a lot more.

## When?

The current release schedule is 'Fairly Soon™' (Q4 2026).

## Core Features

- Best-in-Class precision. 30 Samples: 0.0015mm range, 0.00032mm std dev, 0.000245 average delta.
- **Never calibrate a Z offset ever again.** Where we're going, we don't need offsets.
- Blazingly fast mesh speeds with only a single tap, and accurate on the first try, every try. Powerfully couple it with adaptive mesh for the best results.
- Lets you use the whole bed surface, edge-to-edge. No high spots towards the edge of the bed unlike eddy surface scanners.
- Flawless first layers, every single time. Hit print, and walk away.
- No temperature drift in enclosed printers thanks to continuous tare
- Always reads the true zero point of your bed, accounting for texture and thickness properly.
- Probes your print sheet directly, accounting for damaged PEI and the likes.
- Won't damage your print sheets. Low probe force and 140-170C probe temperature.
- Works on **any** surface (smooth/textured PEI, glass, metal, etc.)

## Extra Features

- Native Kalico integration without plugins, and with strong community support.  
  Not running Kalico? Now's a [great chance to migrate](https://docs.kalico.gg/Migrating_from_Klipper.html).
- Automatic dirty nozzle detection
- Slightly higher probe force accounts for ooze from the nozzle to squish it out of the way, and preventing it from skewing readings
- Built-in nozzle cleanup macros, or bring your own gcode
- Advanced noise filtering and bowden tube compensation
- Fine tune further by reading how much your nozzle grows from thermal expansion, it's that sensitive.
- Far greater fault tolerance than eddy contact probes for Z=0 finding
- Future capabilities to read filament pressure build-up will unlock:
  - Clog detection
  - Max flow rate calibration
  - Automatic pressure advance calibration

## Specs

- E3D Revo compatible
- V6/Volcano supported with a Hemera heat break
- Standalone USB module (STM32)
- 2kHz sampling rate
- Average ~100-300g of force applied to the print surface (configurable in Kalico)
- Operating temperatures:
  - PCB rated for 80C max temperature
  - Load cell rated to 150C

## Toolhead Support

Initial support for Amplify will launch with Stealthburner and AntHead. It will be a community effort to port Amplify to other toolheads. The primary focus is on toolheads for larger Voron machines, such as:

- Stealthburner
- [AntHead](./Toolheads/AmpHead)

Want to contribute your own? Join the [Voron Discord](https://discord.com/channels/460117602945990666/1526211393718587433) thread.

## Sponsors

Development on Amplify started way back in February 2024. This project could not have gotten as far as it has without the help of two amazing sponsors:

- LDO Motion
- Fabreeko

## Contributors

So many awesome people have helped me along in this adventure. You know who you are.

## License

Amplify is fully open source hardware, releasing under the CERN Open Hardware License 2.0 (Weakly Reciprocal).

All source files will be uploaded once the project is out of beta, as they are currently subject to change.
Source will include:

- Bill of Materials
- CAD source including parametric timeline history
- KiCAD PCB design files
- Schematics and technical drawings
- Strain gauge sensor specifications

----

![A Voron Community Project](/Assets/voron-community.svg)

