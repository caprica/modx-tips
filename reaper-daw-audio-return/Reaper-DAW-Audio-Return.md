# DAW Audio Return

## Context

With the default setup for `MIDI Record on DAW`, when you press a key on the MODX+ it will send MIDI data to the DAW.

With correct routing inside the DAW track editor, you ordinarily would send this MIDI back to the MODX+ so that it both records in the DAW track and then emits sound when it arrives back in the MODX+.

As long as the `Direct Monitor` setting remains enabled, this will work.

You *must* still route the MIDI track back to the MODX+, otherwise there will be silence.

*This shows that the direct monitor must be monitoring the incoming MIDI from the DAW and not the outgoing MIDI from the MODX+.*

Almost all guides will tell you to turn this setting off. If you do this, then you will *not* hear any sound output from the MODX+ even though it correctly receives the MIDI data from the DAW.

## Audio Return Track

If you do not want to keep the direct monitor enabled, and really do need the audio from the DAW to be sent to the MODX+ for output, you need to create a supplemental audio (not MIDI) track.

Arm this audio track and set the input to be `Input: Stereo` -> `USB Main L / USB Main R`.

If you do not want to record this audio track, right-click the arm/record button for this track and select `Record: disable (input monitoring only)`.

This will send the audio from the DAW to the master output (which will likely be the MODX+, but depends on configuration).

There may be *a perceptible lag* between key press on the MODX+ and hearing the sound from the MODX+ when doing this.

If you want to hear arpeggios with this setup, you must choose the quick setting preset `Arp Record on DAW`.
