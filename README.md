# Mnisk for macOS

Mnisk turns a display into a listening room for Apple Music and Spotify. Album colours light the edges of a black screen and the record sleeve. Lyrics follow the player clock. A compact transport shows elapsed and remaining time.

**[Download Mnisk 6.5](./Mnisk.zip?raw=true)** for Apple silicon or Intel. The app requires macOS 14 or later. Music-reactive lighting requires macOS 14.2 or later.

## First listen

1. Quit an older copy of Mnisk with **⌘Q**. Unzip the download, drag **Mnisk.app** into **Applications**, then open that copy.
2. Start a track in the Apple Music or Spotify desktop app. Allow Automation for the player you use. **Now Playing** shows artwork, lyrics, progress and playback controls.
3. Press **⌘,** and open **Audio**. Enable **Analyze system audio**, grant the requested system audio recording permission, and check for **Audio detected** during a loud passage.
4. Choose **Animation → Music Reactive**, then open **Ambient Display** from the waveform menu. Press **Escape** to leave.

The downloadable build is ad-hoc signed and has not been notarized. If macOS asks for review on first launch, follow Apple’s instructions for a downloaded app you trust. [Apple’s guide to opening downloaded apps](https://support.apple.com/en-us/102445)

## Shape the glow

| To change | Where to go |
| --- | --- |
| How the light reacts | **Animation** selects Music Reactive, Bass Reactive, Beat Pulse, Lyric Cue or Static. **Beat Detection** sets the listening profile for Music Reactive. |
| Brightness and reach | **Appearance** controls ambient display brightness, border glow, sleeve glow, thickness and radius. The ambient brightness controls are independent of desktop overlay opacity. |
| Artwork or custom colours | **Colors** selects the album frame, borders or both. Choose Album Palette, a solid colour, a gradient, a saved preset or Border Orbit. |
| A fixed-position palette | Turn off **Rotate colours** for the selected surface. A stationary gradient can still pulse with the music. |
| A quieter presentation | Lower **Animation intensity**, or enable **General → Limit visualizer to 12 fps**. **Lyrics on ambient display** controls the captions. |
| A different monitor | Choose **Lyrics → Visualizer display** for the ambient and lyric windows. **Displays** selects monitors for desktop edge lighting. |

Ambient Display suspends when the desktop locks. **General → Restore visualizer after unlock or wake** controls its return.

## Lyric video and practice

Choose a style under **Settings → Lyrics**, then use **Play lyric video** or **Float video** on Now Playing. **Lonely Sky** features one seated couple overlooking a cabin and alpine lake. **Desert After Dark** and **Moonfall** show empty landscapes. **Desktop Overlay** leaves the sky clear and has its own scenery opacity slider for the landscape, the album sleeve and the small artwork thumbnail. Captions and song information stay readable.

**Word Sync** follows word or syllable timestamps in enhanced LRC and music TTML. The active word or syllable glows in your highlight colour. Untimed lyrics open as a transcript. Automatic lookup considers Music library lyrics, associated imports and LRCLIB. Spotify supplies track identity and playback position. For a local Music file, Mnisk also checks for a .ttml or .lrc with the same basename beside the audio.

- **Import lyrics** in Lyrics settings associates a TTML, LRC or text file with the current recording. **Earlier** and **Later** save a timing adjustment for that recording.
- **Loop this lyric** repeats the timed passage in the connected player. Select **Stop lyric loop** to continue.
- **Tap first word** lets you mark actual word starts while the line repeats. **Learn words from loop** can match one pass of up to 25 seconds against the lyric using on-device Speech Recognition. **Align from audio file…** accepts a local copy of the same recording. Matched words are labelled as estimates.

## Singing and word highlights

Choose **Settings → Animation → Lyric Cue** and enable **Audio → Analyze system audio**. Mnisk uses the built-in sound classifier to detect singing, rap, humming and choir. During instrumental passages it measures the background spectrum. During detected singing it uses the remaining energy in the vocal range to drive the glow. Animation settings show when singing is detected. This works without lyric text. Dense mixes, solo instruments that resemble a voice, and the classifier’s half-second listening window can affect the response.

Word-timed TTML and enhanced LRC give the most precise first-play highlights. For line- or phrase-timed lyrics, turn on **Settings → Lyrics → Word Sync → Match sung words on this Mac** and allow Speech Recognition. Mnisk can align an accessible local Apple Music file or follow the captured stream on-device. A **Live word match** briefly marks a word the recognizer has just reported. Recognition can arrive late or miss a word. Confirmed complete lines are saved for replay as **Aligned words · estimated**. Uncertain matches, rests and instrumental sections leave the text neutral. Audio analysis and Speech Recognition have separate permissions.

## Troubleshooting

| What you see | What to check |
| --- | --- |
| Track details appear but the glow stays steady | Check **Audio detected** while the song plays. Try **All playing applications** and **All outputs** if an app-specific tap is silent. Verify **Music Reactive**, a nonzero **Animation intensity**, and that animation is unpaused. System Reduce Motion holds the ambient lighting steady. |
| The tap reports a permission or device error | Review the system audio recording permission for Mnisk in macOS Privacy & Security. Reconnect the selected output or select **All outputs**, then choose **Retry audio capture**. Selecting an analysis output keeps the Mac’s playback routing intact. |
| Audio is detected but the track is missing | Enable the player under **Audio** and allow Automation for that player. System audio and song identification use separate permissions. |
| Cover artwork appears late | Mnisk retries while the track is selected. For local Music files it can also read the embedded cover. Streams with no artwork from the player may still show the fallback sleeve. |
| The room looks too dim | Choose **Appearance → Restore ambient brightness**. A quiet passage leaves a visible baseline, with brightness available for the next beat. |
| The lyrics follow a different version or lack word timing | Import lyrics for that specific recording. Choose a word-timed source for authored word highlights, or use the loop and tap controls. |

## Privacy

The native Core Audio tap analyzes playback on your Mac. It uses neither the microphone nor screen images and leaves normal playback volume and output routing under macOS control. Optional word recognition runs on-device and requires Speech Recognition permission. A requested loop pass is held in memory. Mnisk saves the accepted timing.

Online lyrics lookup sends track title, artist, album and duration to LRCLIB. Spotify artwork may be fetched from the player’s artwork URL. Choose **Imported files** or **Music library** for local-only lyric lookup. Settings, profiles, imported lyrics and per-recording timing live on your Mac.
