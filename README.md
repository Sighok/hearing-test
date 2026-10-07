# Tone Threshold Test

A single-file web page (`index.html`) that measures your hearing threshold for pure tones at chosen frequencies (e.g. 500 Hz and 1000 Hz) and reports the dB difference between them.

Open `index.html` in a browser, set your volume with the reference tone, pick frequencies and an ear, and press **Start test**. Press the button or the space bar every time you hear a tone.

## How it works

- Tones are generated with the Web Audio API (sine, 25 ms ramps, optional pulsing), panned to the left or right ear.
- Thresholds use the modified Hughson–Westlake procedure: down 10 dB after a response, up 5 dB after a miss. The threshold is the lowest level heard on 2 ascending presentations. A fine 4/2 dB mode is available.
- Levels are in dBFS (relative to digital full scale). A browser can't know the absolute loudness of your headphones, so absolute dB HL is not available, but **differences between frequencies are valid as long as the system volume stays fixed**.
- Results show each frequency's threshold relative to a reference frequency, next to the typical difference for normal hearing from the ISO 226:2003 threshold curve.

## Limitations

- Headphone frequency response adds directly to the measured difference (often ±5 dB).
- Test–retest variability is about ±5 dB; use **Retest** to average several runs.
- This is not a medical test.
