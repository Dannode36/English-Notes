# Effect List

- - -

  

Effects are the fourth column of each channel, used to modify notes currently played.

Each effect is followed by a parameter, "xx", from 00-99, which controls the intensity of the effect.  
Some effects have 2 parameters, written as "xy", these are instead in hexadecimal, from 00-FF to offer greater range for a single digit.

Below is a list of all the effects in WaveTracker

  

| Effect                                             | Description                                                                                                                                                                                                                                      |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 0xy - Arpeggio  <br>(first note, second note)      | Cycles through notes in a chord every tick, with base + x and base + y semitones. Use 000 to disable.  <br>For example: 047 defines a major chord                                                                                                |
| 1xx - Note rise  <br>(speed)                       | Continuously increase the pitch at speed xx. Use 100 to disable                                                                                                                                                                                  |
| 2xx - Note fall  <br>(speed)                       | Continuously decrease the pitch at speed xx. Use 200 to disable                                                                                                                                                                                  |
| 3xx - Portamento/Glide  <br>(speed)                | Automatically glide between notes at speed xx. Use 300 to disable                                                                                                                                                                                |
| 4xy - Vibrato  <br>(speed, depth)                  | Modulates pitch with speed x and depth y. Use 400 to disable                                                                                                                                                                                     |
| 7xy - Tremolo  <br>(speed, depth)                  | Modulates volume with speed x and depth y. Use 700 to disable                                                                                                                                                                                    |
| 8xx - Pan  <br>(position)                          | Sets the stereo panning of the channel with position xx.  <br>00 is 100% left  <br>50 is center  <br>99 is 100% right                                                                                                                            |
| 9xx - Stereo split  <br>(phase)                    | Artificially widens the channel in the stereo field by offsetting the phase of one side xx percent. Use 900 to disable.                                                                                                                          |
| Axx - Volume fade down  <br>(speed)                | Continuously decreases the channel volume by xx steps every tick.                                                                                                                                                                                |
| Wxx - Volume fade up  <br>(speed)                  | Continuously increases the channel volume by xx steps every tick.                                                                                                                                                                                |
| Bxx - Jump to frame  <br>(frame #)                 | Jumps the playhead to frame xx. Used to create song loops.                                                                                                                                                                                       |
| Cxx - Stop                                         | Stops the song. (xx has no effect)                                                                                                                                                                                                               |
| Dxx - Skip  <br>(row #)                            | Skips to the next frame at row xx.                                                                                                                                                                                                               |
| Fxx - Tempo change  <br>(ticks/frame)              | Overrides the initial song speed with xx ticks per row.                                                                                                                                                                                          |
| Gxx - Delay  <br>(ticks)                           | Delays the channel's row by xx ticks.                                                                                                                                                                                                            |
| Hxy - Channel Filter  <br>(cutoff, resonance)      | Applies a low pass filter on the output of the channel.  <br>x controls the filter cutoff from 0-F, with 0 being completely open, and F being the most muted.  <br>y controls the resonance of the filter cutoff point.  <br>Use H00 to disable. |
| Ixx - Wave blend  <br>(blend amount)               | Blends the channel's wave with the next wave in the wave bank. xx controls the amount to blend in. 00 is the original wave, 99 is the next wave                                                                                                  |
| Jxx - Wave stretch  <br>(stretch amount)           | Stretches the shape of the channel's wave from the edges inwards. Acts a bit like a pulse-width modulator. xx controls the amount to stretch.                                                                                                    |
| Mxx - Wave FM  <br>(intensity)                     | Frequency modulation. Modulates the channel's wave by the next wave in the wave bank.                                                                                                                                                            |
| Kxx - Wave Sync  <br>(intensity)                   | Increases the speed of the channel's wave during the wave's cycle                                                                                                                                                                                |
| Pxx - Fine pitch  <br>(offset)                     | Detunes the current channel. Default is P50.                                                                                                                                                                                                     |
| Qxy - Note bend up  <br>(speed, semitones)         | Bends the current note up by y semitones at speed x.                                                                                                                                                                                             |
| Rxy - Note bend down  <br>(speed, semitones)       | Bends the current note down by y semitones at speed x.                                                                                                                                                                                           |
| Sxx - Delayed cut  <br>(ticks)                     | Cuts the note after xx ticks have passed.                                                                                                                                                                                                        |
| Vxx - Set wave  <br>(wave #)                       | Sets the channel's timbre to wave xx in the wave bank.                                                                                                                                                                                           |
| Xxx - Downsample  <br>(intensity)                  | Downsamples the channel's output by a factor of xx. Results in a lo-fi, bitcrushed sound                                                                                                                                                         |
| Yxx - Start sample offset  <br>(offset percentage) | Makes any samples start a percentage of the way through their lifetime. xx is how far to start in.  <br>For example: Y25 will start the sample 25% of the way in. Y50 will start the sample halfway through.  <br>Use Y00 to disable.            |

- - -

WaveTracker is an open source music software by Elias Ananiadis / squiggythings · [Source code](https://github.com/squiggythings/WaveTracker)