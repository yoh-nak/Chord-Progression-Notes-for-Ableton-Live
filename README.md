# Chord Progression Notes

**Chord Progression Notes** is a Max for Live chord chart editor and lead-sheet viewer for Ableton Live.

Write, edit, transpose, import, export, and preview chord progressions together with lyrics directly inside Ableton Live.

Version 2.0 introduces a significantly expanded text editor, a detachable editing window with bidirectional synchronization, native file dialogs, and improved support for multiple chord chart formats.

Chord Progression Notes is designed for songwriting, arranging, practicing, rehearsing, and keeping musical references organized within your Live Set.

## Features

### Chord Chart Editor

- Edit, Split, and Preview modes
- Lead-sheet style chord and lyric preview
- Real-time preview updates
- Independent editor and preview scrolling
- Chord-only sections
- Section headings and song metadata
- Independent editor and preview transposition
- Transposition range from -12 to +12 semitones
- Slash chord transposition
- Adjustable editor and preview font sizes
- Word Wrap ON/OFF
- Line number display
- Cursor position display
- Text search
- Find Next / Previous
- Find and Replace
- Replace All
- Table of Contents (TOC)
- Section navigation
- Keyboard shortcuts

### Detachable Editor Window

- Open the editor in a separate floating window
- Edit chord charts without occupying the main Device View
- Bidirectional text synchronization
- Synchronized chord chart content and input format
- Independent editing and preview controls
- Resizable editing window
- Edit, Split, and Preview layouts
- File operations available from both interfaces

Changes made in the floating window are reflected in the Device View, and vice versa.

### File Management

- Open external chord chart files
- Save existing files
- Save As to a specified location
- Native file selection and save dialogs
- Drag-and-drop file loading
- Automatic format detection
- Automatic format switching when loading supported files
- Preserve the original file extension when applicable
- Ableton Live project folder integration
- File operations from both the Device View and floating editor

For new documents, the device can use the saved Live Set's project location as the default save destination.

If the Live Set has not been saved, the normal file dialog is used instead.

Existing external files can be saved back to their original locations.

### Interface

- Compact Device View layout
- Expanded editing workspace in the floating window
- Independent editor and preview font-size controls
- Adjustable text wrapping
- Collapsible Find and Replace controls
- Optional line numbers
- TOC-based section navigation
- Independent editor and preview transposition controls

## Supported Formats

Chord Progression Notes supports four input formats:

- **ChordPro**
- **Chord Over Lyrics**
- **MusicXML**
- **ABC notation**

The appropriate format can be selected manually or detected automatically when loading a supported file.

Each format is parsed into a readable chord-and-lyrics lead-sheet preview.

MusicXML and ABC support is intended for simplified lead-sheet extraction rather than complete musical score rendering.

## ChordPro

ChordPro is the primary format supported by Chord Progression Notes.

The editor supports song metadata, embedded chord symbols, lyrics, section headings, and section delimiters.

### Example

~~~text
{title: After the Rain}
{artist: Example Artist}
{key: D}
{tempo: 112}
{time: 4/4}

{start_of_section: Intro}
[D] [A] [Bm] [G]
{end_of_section}

{start_of_verse: Verse 1}
[D]Morning light is falling [A]softly
[Bm]Through the curtains by my [G]bed
{end_of_verse}

{start_of_chorus: Chorus}
[D]Stay with me after the [A]rain
[Bm]Nothing has to feel the [G]same
{end_of_chorus}

{start_of_bridge: Bridge}
[Em]Everything is [G]changing
[A]But we carry [D]on
{end_of_bridge}
~~~

### ChordPro Directives

Supported section delimiters include:

~~~text
{start_of_section}
{end_of_section}

{start_of_verse}
{end_of_verse}

{start_of_chorus}
{end_of_chorus}

{start_of_bridge}
{end_of_bridge}

{start_of_intro}
{end_of_intro}

{start_of_tab}
{end_of_tab}

{start_of_grid}
{end_of_grid}
~~~

Common abbreviated closing directives such as `{eov}`, `{eoc}`, and `{eob}` are also recognized.

ChordPro metadata directives such as title, artist, key, tempo, and time signature are displayed in the lead-sheet preview.

## Chord Over Lyrics

Chord Over Lyrics is supported for conventional text-based chord charts.

### Example

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

Chord symbols and lyrics are displayed as a readable lead sheet.

## MusicXML

MusicXML files can be opened or pasted into the editor.

The device extracts information useful for chord-and-lyrics display, including:

- Song title
- Composer / artist
- Key
- Tempo
- Time signature
- Harmony / chord symbols
- Lyrics
- Section labels

MusicXML support focuses on extracting musical information for a simplified lead sheet.

It does not attempt to reproduce a complete engraved score.

Uncompressed `.musicxml` and `.xml` files are supported. Compressed `.mxl` files are not supported.

## ABC Notation

ABC notation is supported for extracting chords, lyrics, and basic song information.

Chord symbols written using quoted chord names and lyrics written with `w:` lines can be converted into a simplified lead-sheet preview.

### Example

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

ABC support is focused on chord-and-lyric references rather than traditional score rendering.

## Editor Features

Version 2.0 significantly expands the text editing capabilities.

### Find and Replace

Use the Find controls to search through chord chart text.

Available operations include:

- Find
- Find Next
- Find Previous
- Replace
- Replace All

The search interface can be shown or hidden when needed.

### Line Numbers

Use the Lines button to show or hide line numbers.

This is useful when working with longer chord charts or structured text formats.

### Word Wrap

Use Wrap to switch between wrapped and unwrapped text.

Word wrapping can be configured independently for the editor and preview.

### Font Size

The editor and preview have independent font-size controls.

Use the `-` and `+` controls to adjust text size.

### Table of Contents

The TOC function provides navigation between recognized song sections.

Typical sections include:

- Intro
- Verse
- Pre-Chorus
- Chorus
- Bridge
- Interlude
- Solo
- Outro

Selecting a recognized section allows faster navigation through longer songs.

### Keyboard Shortcuts

Common editor shortcuts include:

| Shortcut | Function |
|---|---|
| Ctrl + F | Find |
| Ctrl + H | Find and Replace |
| F3 | Find Next |
| Shift + F3 | Find Previous |
| Ctrl + O | Open file |
| Ctrl + S | Save |
| Ctrl + Shift + S | Save As |

File shortcuts use the corresponding Max file-handling functions.

## Detachable Editor

Click **Open Editor** in the Device View to open a separate editing window.

The floating editor provides a larger workspace for editing and previewing chord charts.

Both interfaces share the same chord chart content.

### Bidirectional Synchronization

Editing text in the Device View updates the floating editor.

Editing text in the floating editor updates the Device View.

This allows the compact Device View to remain available while more extensive editing takes place in the separate window.

The floating window also includes file management, transposition, search, and text editing controls.

## File Import and Export

### Open

Use Open to select a chord chart from your computer.

Supported files can also be loaded using drag and drop.

The device attempts to detect the input format automatically and switches to the corresponding editing mode.

### Save

Use Save to save the current document.

If the document was opened from an external file, Save uses its existing file path.

For a new document, the device can use the saved Live Set's project folder as its default destination.

### Save As

Use Save As to select a different file name or destination.

When available, the current Live project folder is used as the initial location.

You can select another folder through the native file dialog.

### File Extensions

The editor attempts to retain the extension of the currently opened file.

For new documents, a suitable extension is selected according to the active format.

Common extensions include:

| Format | Extensions |
|---|---|
| ChordPro | `.cho`, `.chopro`, `.chordpro` |
| Chord Over Lyrics | `.txt` |
| MusicXML | `.musicxml`, `.xml` |
| ABC notation | `.abc` |

## Usage

1. Add `Chord_Progression_Notes_v2.0.amxd` to an Ableton Live track.
2. Select the appropriate format, paste text, or open an existing file.
3. Choose an editing mode:
   - **Edit** — Text editor only
   - **Split** — Editor and preview
   - **Preview** — Lead-sheet preview only
4. Click Open Editor if you prefer working in a separate window.
5. Use the editor tools to search, replace, navigate, and organize the text.
6. Use the transpose controls to change chord symbols.
7. Save your chord chart using Save or Save As.

## Editor Transpose

Editor Transpose directly modifies chord symbols in the source text.

Use the `-` and `+` buttons to transpose chord symbols by semitone.

For example:

~~~text
C | Am | F | G
~~~

Transposed up by two semitones:

~~~text
D | Bm | G | A
~~~

Slash chords are also supported.

Example:

~~~text
G/B
~~~

Transposed up by two semitones:

~~~text
A/C#
~~~

Because Editor Transpose modifies the underlying text, the result becomes the new working chord progression.

## Preview Transpose

Preview Transpose changes only the rendered lead sheet.

The original editor text remains unchanged.

Use the `-`, `0`, and `+` controls to transpose the preview from -12 to +12 semitones.

The `0` button resets preview transposition.

This makes it possible to compare different keys without permanently editing the original chord chart.

## Independent Transposition

Editor Transpose and Preview Transpose operate independently.

For example, the editor may contain:

~~~text
C | Am | F | G
~~~

With Preview Transpose set to +2, the preview displays:

~~~text
D | Bm | G | A
~~~

while the editor still contains:

~~~text
C | Am | F | G
~~~

If Editor Transpose is then increased by two semitones, the underlying source text becomes:

~~~text
D | Bm | G | A
~~~

This becomes the new base progression for the preview.

## Requirements

- Ableton Live 12
- Max for Live

A compatible version of Max must be available through Ableton Live.

## Installation

Download:

~~~text
Chord_Progression_Notes_v2.0.amxd
~~~

Place the device in your Ableton Live User Library or preferred Max for Live device folder.

Drag it onto a track in Ableton Live.

The device is distributed as a single `.
