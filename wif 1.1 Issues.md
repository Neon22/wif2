# wif1.1 Issues
A summary of issues with the existing 1.1 spec. Specifically this document is not here to discuss the history or story of the format but just what is needed to generate an improved, more uptodate, supportable version.

# Summary:
First of all it exists and has enabled design file interchange since 1997.
It has a number of weaknesses which have been discovered since its inception. Some of these are in the design and some as a result of how people have come to use the format to get work done.

- the file carries the most important data defining the weaving strucure (but not all info).
- it does not carry information about a specific final fabric design - e.g. epi/ppi

# Size and compression
The format was designed with a single compression feature. This identifies the most common value in each section. This value is used for any index which is omitted.
E.g. If the warp is 90% black threads then a single entry defines the default as black. So 90% of the warp threads do not need to be listed in the file. Only those threads that are not black appear in the associated section with their index into the color section.

This was useful to reduce file sizes in 1997. This is less of an issue now.
The unfortunate side effect is that simple text editing of the file is made more complex because there is not always a simple list of index, value pairs. Copy and paste operations are made more difficult if his mode is used.

# Order of sections
When computers had little RAM then the order of parsing elements could have a significant impact on importing the file. This is no longer the case. The entire file can be consumed and processed simply. There is no longer a need for a specific processing order. 
 - This may not be true for computer dobby controllers.
  - An internal manifest is a duplication of information and not really required.

# Usecases:
 - Transferring files between systems
   - this works adequately because the file carries the most important data defining the weaving strucure
 - Controlling a computer dobby loom
   - some standalone dobby controllers use the format to control a loom.
   - some have visual feedback showing the proposed state of the loom and current position in the sequence.
 - hand editing a file  (or using a dedicated software tool)
   - to manipulate the warp/weft/color aspects of the draft directly.
   - made difficult if the simple size reduction scheme is enabled.

# Weaknesses:

- Allow cut and paste editing of files is inhibited if compressed.
- Differeniate between general design information and a specific piece of cloth.
  E.g. 
  - epi/ppi
  - variable denting
  - Yarn dtails other than simply color
- Enable enough optional sections so the file can be a principle weaving software file. Not purely for interchange.
  
