# Wavelight

Wavelight is a stereo master tuning insert. It shifts a finished mix by a fixed musical interval and leaves the tempo and the length of the audio alone.

The default interval takes A4 from 440 Hz to 444 Hz. That is 15.67 cents (`1200 × log2(444 / 440)`). A 220 Hz tone comes out at 222 Hz. Reference is the A4 the music was tuned to. Tune is the shift in cents. The large readout is reference times that ratio, so 440 Hz and +15.67 cents reads 444 Hz.

![Wavelight, with the wave, the 444 Hz readout, and the tuning row](screenshots/interface.png)

The wave is artwork. It moves with the music. The tuning is the fixed interval.

## Controls

![Reference, tune, output, bypass, and the output meters](screenshots/controls.png)

| Control | What it does |
| --- | --- |
| Reference | The A4 the incoming music is tuned to, from 420 Hz to 480 Hz. Default 440 Hz. |
| Tune | The shift, from −200 cents to +200 cents. Default +15.67 cents. |
| Output | The resulting A4, in hertz. The arrows step it by 1 Hz. |
| Bypass | Crossfades to a dry copy delayed by the same amount as the tuned path, so the timing stays put. |
| Level | Output trim, from −24 dB to +12 dB. |

Programs are **444 Hz**, **Unity**, and **432 Hz**. Unity is no shift. 432 Hz is 440 Hz moved down to 432 Hz.

## Where it runs

On Akai Professional MPC standalone it is a master insert, for MPC OS 3.10.1 and later. Copy the plugin folder into `VST2 Plugins` on the internal drive, an SD card, or a USB drive, with External Plugin Support turned on. The install steps are in Download.

On macOS it is a VST® 3 plug-in, an Audio Unit, and an Audio Unit app extension (AUv3). The minimum system is macOS 12. The manufacturer code is Wylt and the plug-in code is WY1S.

Manufacturer and plug-in name are both Wavelight.

## Download

[Wavelight 1.0.0 for macOS](https://github.com/asearan/Wavelight/releases/download/v1.0.0/Wavelight-1.0.0-macOS.pkg) is a signed installer for Apple silicon. It needs macOS 12 or later. The installer adds the VST® 3 plug-in, the Audio Unit, and the Wavelight app. Open the app once so macOS registers the Audio Unit app extension.

The package is signed with an Apple Developer ID certificate. This build is not notarized, so the first time you open the downloaded installer, macOS asks you to approve it.

[Wavelight 1.0.0 for MPC](https://github.com/asearan/Wavelight/releases/download/v1.0.0/wavelight-1.0.0-mpc.zip) is for MPC OS 3.10.1 and later, the firmware that loads third-party plugins from a `VST2 Plugins` folder. The zip contains the 32-bit and 64-bit builds and an `INSTALL.txt`.

1. Update the MPC to 3.10.1 or later. Preferences, Info shows the version.
2. Open Preferences, Enhancements. Turn on Enable Enhancements and External Plugin Support. Wait a few seconds, then restart.
3. Unzip the download and copy the folder `Wavelight - VST - Wavelight` into a folder named exactly `VST2 Plugins` at the top of the internal drive, an SD card, or a USB drive.
4. Keep the folder name as it is. It should contain `plugin.json`, `version.xml`, `Plugin Skins`, and `VST`.
5. Restart the MPC if Wavelight does not appear, then add it as an insert under External Plugins.

Save the project first. A plugin runs inside the MPC software, so a fault can freeze or restart the machine. Akai Professional and inMusic do not support third-party plugins.

## Trademarks

Wavelight is an independent product. The names below identify the instruments and formats it runs on. The header mark on the screen is the Retroloop logo.

Akai Professional and MPC are trademarks of inMusic Brands, Inc., registered in the U.S. and other countries.

VST® is a registered trademark of Steinberg Media Technologies GmbH.

<img src="screenshots/vst-compatible.png" width="280" alt="VST Compatible. VST is a registered trademark of Steinberg Media Technologies GmbH.">

macOS and Audio Units are trademarks of Apple Inc., registered in the U.S. and other countries.

JUCE is a trademark of Raw Material Software Limited. The macOS plug-in is built with JUCE 8.

The VST Compatible logo is Steinberg’s artwork, shown unaltered. Wavelight does not use the Akai Professional logo.

All other product names, company names, and marks belong to their respective owners.

Copyright © Wavelight. All rights reserved.
