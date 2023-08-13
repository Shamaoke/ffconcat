**ffconcat**

````
ffconcat -i INPUT -t TITLE -m METADATA OUTPUT
````

Concatenate multiple audio files of some audio format into one Opus format audio file with chapters and metadata.

# Options #

**-i**, **--input**, **--input=**

  Specify input files.

**-t**, **--title**, **--title=**

  Specify a common heading for chapters. Each chapter will have this heading, plus
  the chapter number in order.

**-m**, **--metadata**, **--metadata=**

  Specify the metadata to include in the output file. Specified metadata must
  have the following format: `'NAME=VALUE; NAME=VALUE; NAME=VALUE ...'`, i. e.
  a list of name-value pairs in quotes separated by a semicolon.

# Examples #

````
ffconcat -i 'assets/caps/16b/*.webm' \
         -t 'Lesson 16. Section B. Drills' \
         -m 'TITLE=Lesson 16. Section B. Drills; ALBUM=Japanese: the Spoken Language; ARTIST=Eleanor Harz Jorden; ARTIST=Mari Noda' \
            output.opus
````

