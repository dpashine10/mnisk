# Mnisk for macOS

Mnisk brings Apple Music and Spotify playback, album-coloured lighting and synchronized lyrics to your Mac. Open Now Playing to see your track, float the lyrics beside another app, or turn a display into a listening room with an illuminated sleeve, lyrics, transport and a needle meter.

**[Download Mnisk 6.3 for macOS](./Mnisk.zip?raw=true)**

## Install

1. Download and unzip Mnisk. If you are updating, quit the running copy with **⌘Q**.
2. Drag **Mnisk.app** into **Applications** and open it there. Mnisk appears in the Dock and the **⌘Tab** app switcher. Its waveform menu also gives you quick access while another app is in front.
3. Play a song in the Apple Music or Spotify desktop app. Allow Automation access for each player you want to connect.
4. Open **Settings** in Now Playing or press **⌘,**. In **Audio**, enable system audio analysis if you want beat-reactive lighting. The native Core Audio tap analyzes samples locally.

The universal app supports Apple silicon and Intel Macs running macOS 14 or newer. System audio analysis requires macOS 14.2 or newer. This build has an ad-hoc signature and has not been notarized by Apple. macOS may ask you to review it on first launch. [Apple’s guide to opening downloaded apps](https://support.apple.com/en-us/102445)

## Lyrics

Choose **Settings → Lyrics → Word Sync**, then **Play lyric video**. Word-timestamped lyrics put the accent on the sung word. Completed words settle back to neutral, and the remaining words stay legible. Mnisk also uses those cues in Ambient Display.

If the display says **Line timing**, the source supplied one timestamp per line. Under **Settings → Lyrics → Word timing**, you can tap each word as it starts, or choose **Align from audio file…** with a local audio copy of the same recording. Alignment uses Apple’s on-device recognizer and requires Speech Recognition permission and a supported system language. It labels matched lines as estimates. Singing, backing vocals and noise can prevent a confident match. Enhanced LRC and music TTML can supply original word timestamps. For local files in Apple Music, Mnisk also checks a same-named .ttml or .lrc alongside the audio file. A timestamped phrase retains its supplied timing until refined. Plain text is available as a transcript.

Automatic lookup can use Music library lyrics, an associated local LRC file and LRCLIB. Spotify provides the recording identity and playback clock. For a specific version of a song, import its LRC file while that recording is selected. **Earlier** and **Later** adjust the offset for that recording.

LRCLIB lookup sends the recording title, artist, album and duration. Choose **Imported files** or **Music library** in Lyrics settings for local-only lyrics lookup.

## Night landscapes

Open **Settings → Lyrics**, choose **Lonely Sky**, **Desert After Dark** or **Moonfall**, then select **Play lyric video** or **Float video** on Now Playing. Two seated couples look out over a cabin and alpine lake, desert mesas or a moonlit waterfall. You can turn down movement and detail or use Reduce motion.

## Repeat a lyric

Select **Loop this lyric** during a timed line to repeat that passage in Apple Music or Spotify. **Stop lyric loop** returns to regular playback. You can pause, resume or switch windows while practicing.

If your lyrics have line timestamps, you can use **Tap first word** and mark each word while the line repeats. Or enable **Audio → Analyze system audio**, start a lyric loop and choose **Learn words from loop**. This uses one pass of up to 25 seconds of the selected audio source, processed on-device with Speech Recognition permission. Mnisk saves word times for successful matches. No audio file is saved. When a recording cannot be matched, the original line or phrase timing remains available.

## Lighting

- **Fixed borders:** Open **Settings → Colors**, choose **Screen borders** or **Frame and borders**, and turn off **Rotate colours**. Brightness can still follow the music.
- **Lyric Cue:** Select it in **Settings → Animation**. The glow responds to timestamped words, phrases or lines during playback, including in Ambient Display.
- Open **Ambient Display** in the waveform menu. The border and sleeve frame use your selected lighting palettes. The faceplate shows artwork, track information, transport and lyrics. Enabling audio analysis adds a signal-level meter. Press **Escape** to leave.
- To change the ambient lights, open **Settings → Appearance**. Adjust **Ambient display brightness**, **Ambient border glow** and **Album frame glow**, or choose **Restore ambient brightness**. For the same moving palette on the edges and sleeve, choose **Frame and borders → Album Palette** and enable **Rotate colours** in Colors. Toggle ambient lyrics under **General**. Mnisk suspends the display when macOS locks.
- **Profiles:** Save a combination of lighting and lyric styles in **Settings → Profiles**, then reuse it or associate it with a recording.
