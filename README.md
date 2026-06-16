# MP3 Tag Reader in C

## Project Overview

The MP3 Tag Reader is a command-line application written in C that reads and displays metadata stored in MP3 audio files using the ID3v2 tag format. The project demonstrates file handling, binary data processing, string manipulation, and structured programming concepts.

The application extracts important information such as song title, artist, album, genre, year, and comments directly from MP3 files without playing the audio.

---

## Features

✅ Read ID3v2 tags from MP3 files

✅ Display Song Title

✅ Display Artist Name

✅ Display Album Name

✅ Display Genre

✅ Display Year of Release

✅ Display Comments

✅ Binary file processing

✅ Error handling for invalid MP3 files

✅ User-friendly command-line interface

---

## Technologies Used

* C Programming Language
* GCC Compiler
* File Handling
* Binary File Processing
* Structures
* Dynamic Memory Management
* Linux/Unix Environment

---

## Project Structure

```text
MP3_Tag_Reader/
│
├── main.c
├── editor.c
├── reader.c
├── id3.h
├── reader.h
├── editor.h
├── Makefile
└── README.md
```

---

## Supported ID3 Tags

| Tag  | Description |
| ---- | ----------- |
| TIT2 | Song Title  |
| TPE1 | Artist Name |
| TALB | Album Name  |
| TYER | Year        |
| TCON | Genre       |
| COMM | Comments    |

---

## Functionalities

### View MP3 Tags

Displays metadata information stored in the MP3 file.

```bash
./mp3_tag_reader -v song.mp3
```

Example Output:

```text
----------------------------------
MP3 TAG READER
----------------------------------
Title   : Believer
Artist  : Imagine Dragons
Album   : Evolve
Year    : 2017
Genre   : Rock
Comment : Sample MP3 File
----------------------------------
```

---

### Edit MP3 Tags

Modify metadata information.

```bash
./mp3_tag_reader -e -t "New Title" song.mp3
```

Supported Edit Options:

| Option | Description  |
| ------ | ------------ |
| -t     | Edit Title   |
| -a     | Edit Artist  |
| -A     | Edit Album   |
| -y     | Edit Year    |
| -g     | Edit Genre   |
| -c     | Edit Comment |

Example:

```bash
./mp3_tag_reader -e -a "Rahul Mali" song.mp3
```

---

## Compilation

Compile using GCC:

```bash
gcc *.c -o mp3_tag_reader
```

Or using Makefile:

```bash
make
```

---

## Execution

View Tags:

```bash
./mp3_tag_reader -v sample.mp3
```

Edit Tags:

```bash
./mp3_tag_reader -e -t "My Song" sample.mp3
```

---

## Concepts Covered

### File Handling

* fopen()
* fread()
* fwrite()
* fclose()

### Binary Data Processing

* Reading MP3 frame data
* Extracting ID3 metadata
* Byte-level operations

### Structures

Used for organizing MP3 tag information.

```c
typedef struct
{
    char title[100];
    char artist[100];
    char album[100];
    char year[10];
    char genre[50];
    char comment[200];
} MP3Tag;
```

---

## Algorithm Complexity

| Operation    | Complexity |
| ------------ | ---------- |
| Read Tags    | O(n)       |
| Search Frame | O(n)       |
| Edit Tag     | O(n)       |
| Write Tag    | O(n)       |

Where n represents the size of the MP3 metadata section.

---

## Learning Outcomes

Through this project, I gained experience in:

* Binary file manipulation
* MP3 file structure understanding
* ID3v2 tag processing
* File pointer operations
* String handling in C
* Modular software development
* Error handling and validation

---

## Future Enhancements

* Support for ID3v1 Tags
* Batch MP3 Tag Editing
* Album Art Extraction
* Playlist Generation
* GUI-based MP3 Tag Editor
* UTF-8 Metadata Support

---

## Sample Run

```text
$ ./mp3_tag_reader -v song.mp3

MP3 TAG READER

Title   : Shape of You
Artist  : Ed Sheeran
Album   : Divide
Year    : 2017
Genre   : Pop
Comment : Sample Audio File
```

---

## Author

**Rahul Suresh Mali**

* B.Tech Mechatronics Engineering
* Embedded Systems & Software Development Enthusiast
* C Programming & System Software Developer

---

## License

This project is open-source and available under the MIT License.

# MP3-Tag-Reader
