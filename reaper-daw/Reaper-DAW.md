# Using MODX+ with Reaper DAW

This document describes minimal configuration steps for using the MODX+ keyboard with the Reaper DAW.

The setup will be for a typical DAW workflow, using the MODX hardware as the instrument and Reaper as the sequencer.

After completing this setup:

 * MIDI from the MODX+ can be saved to a MIDI track in Reaper
 * Reaper's MIDI track is routed back to the MODX+ so it can be heard through speakers or headphones
 * Reaper controls the MIDI clock and tempo

## Reaper Setup

### Audio Device

Connect the MODX+ via USB and power it on.

In the main menu, choose `Options` and then `Preferences...`.

In the preferences tree view on the left, find the `Audio` group and within that `Device`.

For the audio system, choose `ASIO`.

For the `ASIO` driver, choose `Yamaha Steinberg USB ASIO`.

Make sure `Enable inputs` is ticked.

![Reaper Audio Device Settings](https://github.com/caprica/modx-tips/raw/master/reaper-daw/reaper-audio-device.png "Reaper Audio Device Settings")

### MIDI Inputs

Still within the `Audio` preferences group, find `Midi Inputs`.

The table of `Midi input devices` should list MODX devices 1 through 3.

Use the context menu or double-click the table cells on the `MODX-1` device to enable `Input`, `All` and `Control`.

![Reaper MIDI Inputs](https://github.com/caprica/modx-tips/raw/master/reaper-daw/reaper-midi-inputs.png "Reaper MIDI Inputs Settings")

### MIDI Outputs

Still within the `Audio` preferences group, find `Midi Outputs`.

The table of `Midi output devices` should list MODX devices 1 through 3.

Use the context menu or double-click the table cells on the `MODX-1` device to enable `Enable` and `Clock`.

![Reaper MIDI Outputs](https://github.com/caprica/modx-tips/raw/master/reaper-daw/reaper-midi-outputs.png "Reaper MIDI Outputs Settings")

## MODX+ Setup

Press `SHIFT` with `UTILITY` to open the `Quick Utilities` page.

Tap `Quick Setup 1: MIDI Rec on DAW`.

![MODX+ MIDI REC ON DAW](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-midi-rec-on-daw.png "MODX+ MIDI Record on DAW Quick Settings")

Alternatively, if you want individual notes of an arpeggio to be sent rather than just the activation key, tap `Quick Setup 2: Arp Rec on DAW`.

![MODX+ ARP REC ON DAW](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-arp-rec-on-daw.png "MODX+ ARP Record on DAW Quick Settings")

Find the `MIDI I/O` settings and ensure (it will be by default) that the `Midi Sync` option is set to `MIDI` (so that the MODX+ will use Reaper's clock).

![MODX+ MIDI SYNC](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-midi-sync-midi.png "MODX+ MIDI Sync")

Depending on how you want to operate, on the `Advanced` settings, set the `MIDI I/O Mode` to `Single` so that all parts are sent on the same channel. This can save you having to map parts to channels and tracks, and is simpler if you record one part at a time. You can choose which MIDI channel to use, but leaving it at the default is fine.

![MODX+ MIDI I/O Mode: Single](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-midi-io-mode-single.png "MODX+ MIDI I/O Mode: Single")

If you want to record multiple parts to mutiple separate MIDI channels, each one becoming a separate track inside Reaper, leave this setting at `Multi`.

![MODX+ MIDI I/O Mode: Multi](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-midi-io-mode-multi.png "MODX+ MIDI I/O Mode: Multi")

If you value your sanity, leave `Direct Monitor` set to `ON` *despite what many guides will tell you*.

![MODX+ MIDI Direct Monitor: Off](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-direct-monitor-on.png "MODX+ Direct Monitor: On")

To prevent Reaper from sending the MODX+ a start song command (which will start the internal sequencer on the MODX+), set the `Receive` option to `OFF` in the `Sync` settings:

![MODX+ Sync Receive: Off](https://github.com/caprica/modx-tips/raw/master/reaper-daw/modx+-sync-receive-off.png "MODX+ Sync Receive: Off")

## See also

* [Reaper DAW Audio Return](../reaper-daw-audio-return/Reaper-DAW-Audio-Return.md)
