# Chord Progression Notes

Chord Progression Notes is a Max for Live device for writing, transposing, and previewing chord progressions together with lyrics directly inside Ableton Live.

It provides a simple text editor and a lead-sheet style preview so you can keep chord charts and lyrics inside your Live Set while composing, arranging, practicing, or rehearsing.

## Features

- Edit, Split, and Preview views
- Lead-sheet style chord and lyric preview
- Independent editor transposition
- Independent preview transposition
- Editor chord transposition from -12 to +12 semitones
- Preview chord transposition from -12 to +12 semitones
- Section headings such as Intro, Verse, Chorus, Bridge, Interlude, and Outro
- Song metadata display
- Chord-only sections
- Independent editor and preview scrolling
- Single `.amxd` file
- No external files required

## Supported Formats

Chord Progression Notes currently supports:

- ChordPro
- Chord Over Lyrics
- MusicXML
- ABC notation

Each format is parsed and displayed as a readable chord-and-lyrics lead sheet.

## ChordPro Example

~~~text
{title: After the Rain}
{artist: Example Artist}
{key: D}
{tempo: 112}
{time: 4/4}

{comment: Verse 1}
[D]Morning light is falling [A]softly
[Bm]Through the curtains by my [G]bed

{comment: Chorus}
[D]Stay with me after the [A]rain
[Bm]Nothing has to feel the [G]same
~~~

## Chord Over Lyrics Example

~~~text
Title: After the Rain
Artist: Example Artist
Key: D
Tempo: 112
Time: 4/4

[Verse 1]

D                         A
Morning light is falling softly
Bm                            G
Through the curtains by my bed

[Chorus]

D                       A
Stay with me after the rain
Bm                          G
Nothing has to feel the same
~~~

## MusicXML

MusicXML data can be pasted into the editor and previewed as a simplified lead sheet.

The device reads information useful for chord-and-lyrics display, including:

- Song title
- Composer / artist
- Key
- Tempo
- Time signature
- Harmony / chord symbols
- Lyrics
- Section labels

MusicXML support is focused on lead-sheet preview rather than full score rendering.

## ABC Notation

ABC notation is also supported.

Chord symbols written with quoted chord names and lyrics written with `w:` lines can be converted into a lead-sheet style preview.

Example:

~~~text
X:1
T:After the Rain
C:Example Artist
M:4/4
Q:1/4=112
K:D

%%text Verse 1
"D"D D "A"A A |
w: Morning light is falling softly

"Bm"B B "G"G G |
w: Through the curtains by my bed
~~~

## Usage

1. Add `Chord_Progression_Notes_v1_1.amxd` to an Ableton Live track.
2. Select the appropriate input format from the `Format` menu.
3. Enter or paste your chord and lyric data into the editor.
4. Use:
   - `Edit` for the editor only
   - `Split` for editor and preview
   - `Preview` for the lead-sheet view
5. Use the editor transpose controls when you want to rewrite the chord data itself.
6. Use the preview transpose controls when you want to temporarily view the progression in another key without changing the editor contents.

## Editor Transpose

The editor transpose controls directly rewrite chord symbols in the editor.

Use the `-` and `+` buttons to transpose the current chord data by semitone.

Example:

~~~text
C | Am | F | G
~~~

transposed up by 2 semitones becomes:

~~~text
D | Bm | G | A
~~~

Slash chords are also transposed.

Example:

~~~text
G/B
~~~

transposed up by 2 semitones becomes:

~~~text
A/C#
~~~

Because editor transposition modifies the actual text, the transposed result becomes the new working chord data.

## Preview Transpose

The preview transpose controls change only the rendered preview.

Use the `-`, `0`, and `+` controls to transpose the preview from:

~~~text
-12 to +12 semitones
~~~

The editor text remains unchanged.

This is useful when you want to quickly test another key without permanently changing the original chord data.

The `0` control returns the preview to the same pitch as the current editor contents.

## Editor and Preview Transpose

Editor Transpose and Preview Transpose are independent.

For example:

~~~text
Editor:
C | Am | F | G
~~~

If the preview is transposed up by 2 semitones, the preview can display:

~~~text
D | Bm | G | A
~~~

while the editor still contains:

~~~text
C | Am | F | G
~~~

If the editor itself is then transposed up by 2 semitones, the editor becomes:

~~~text
D | Bm | G | A
~~~

and that becomes the new base content.

## Notes

Chord Progression Notes is designed primarily as a songwriting and reference tool.

It is not intended to replace a full notation application such as MuseScore, Dorico, Finale, or Sibelius.

MusicXML and ABC support focuses on extracting information useful for chord-and-lyrics lead sheets rather than rendering complete traditional notation.

## Requirements

- Ableton Live 12
- Max for Live

Tested with:

- Ableton Live 12.0.5
- Max 8.6.2

## Installation

Download:

~~~text
Chord_Progression_Notes_v1_1.amxd
~~~

Place the file anywhere in your Ableton Live User Library or Max for Live device folder, then drag it onto a track.

No additional files or external dependencies are required.

## Version

### v1.1

Added separate transpose controls for the editor and preview.

Changes:

- Added Editor Transpose controls
- Moved preview transposition controls to the Preview section
- Editor Transpose directly rewrites chord data
- Preview Transpose leaves the editor text unchanged
- Added preview reset to `0`
- Improved device width and layout
- Preserved support for ChordPro, Chord Over Lyrics, MusicXML, and ABC notation

### v1.0

Initial release.

Supported formats:

- ChordPro
- Chord Over Lyrics
- MusicXML
- ABC notation

## License

Free Max for Live device.
