# wif2
A collection of information about the potential new wif file.

# Features:
Issues we would like to solve, Features we would like to see.
- Allow cut and paste editing of files
  - implies a text based system using lines
- Add features which would enable future loom control machines more control
  - .
- Carry additional information about the design
  - epi/ppi to enable better rendering options


# Type of file:
Needs to be a text based format. We do not need a binary format.
 - enables hand editing, readability, futureproofing.

## Possibilities
 - Yaml
   - most readable of the three. Best at configuration files.
 - Json
  - Second most readable. Good at datafiles.
    - uses {} and indenting to define regions
  - a schema means we can verify correctness of a file.
    - https://json-schema.org/learn/getting-started-step-by-step

 - XML
  - least redable of the three.
    - relies on formatting symbols e.g. <>
  - a schema means we can verify correctness of a file.
  - very capable for complex descriptions (our needs are modest)

