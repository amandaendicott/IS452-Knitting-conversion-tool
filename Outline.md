# Outline for Knitting Conversion Program


This program will focus on lace knitting, (Cables, Brioche, colorwork etc are outside of scope)
I think that my final program will be missing a lot of functionality that would make it actually usable for anyone above a very beginner lace knitter.

A Key of abbreviations and symbols will print at the top of the program.

Abbreviation | Description | Symbol | ASCII
-------------|-------------|------- | ------
k | Knit | |
kfb | knit 1 into front and back of a stitch | |
ksp |	knit 1 stitch, slip this stitch from right needle to left needle, pass second stitch on left needle over first stitch and off left needle; return stitch to right needle | |
k2tog | knit 2 stitches together | |
M1 | make one stitch knitwise | |
M1p | Make one stitch purlwise | |
p | purl | |
pfb | purl into front and back | |
p2tog | purl two together | |
psso | pass slipped stitch over | |
p2sso | pass 2 slipped stitches over | |
SKP | slip 1 knitwise, knit 1, pass slip stitch over knit stich | |
SK2P | slip 1 knitwise, knit 2 together, pass slipt titch over knit 2 together | |
sl | slip | |
sl1k | slip 1 knitwise | |
sl1p | slip 1 purlwise | |
ssk | slip 2 stiches knitwise, knit together through back loops | |
ssp | slip 2 stitches knitwise, return 2 stitches to left needle, purl together though back loops | |
yo | yarn over | |



* Dictionary for conversion
  * Dictionary could be hard coded into program or loaded from file.  Loading from file would make program more universal. Could be applied to other crafts or even other translations. Load from file using JSON?
  * Key:Value = Knitting Stitch:Chart Graphic
  * [Standard knitting abbreviations taken from Craft Yarn Council](https://www.craftyarncouncil.com/standards/knitting-abbreviations)
  * [Knit Chart Symbols](https://www.craftyarncouncil.com/standards/knit-chart-symbols)
    * Unsure how to code symbols as values.  May have to use ASCII values if I can't figure this out. Also, symbols on charts are different depending on right side of fabric or wrong side.  Trying to figure this oout when using a dictionary of key:value pairs may have to disregard. Also symbols are traditionally enclosed in a square 
  
  
* Use switch type statement to allow options for  input of knitting abbreviations.  I'm going to prioritize making reading from a file work and Work on the Manual Entry option as a to be included if time and knowledge allow. 
    1. Manual Entry  - Separated by commas.  Enter starts a new row. prompts to enter next row or type DONE to finish. 
      Will use counter to increase row lines
    1. From File - Allow user to enter filename.  Runs conversion tells user their chart will be named filename_charted
    1. From File - have at least two files already available in program from popular knitting patterns. 
### File 1: Using Feather and Fan scarf pattern

CO: 76 stitches

Row | Stitches
-----|-----
Row 1 | k2, k2tog x 3, [(yo, k1) x 6, k2tog x 6] x3, (yo, k1) x 6, k2tog x 3, k2
Row 2 | Purl
Row 3 | Knit
Row 4 | Purl

### File 2: Zig Zag Lace

CO: in multiples of 11 + 6

Knit first and last 3 stitches for garter edge

Knit 4 rows at beginning and before bind off. 

Row | Stitches
-----|-----
R1 | * p1, yo, k7, k2tog, p1*
R2 | and all even-numbered rows 2-32: *k1, p9, k1*
R3 | * p1, k1, yo, k6, k2tog, p1*
R5 | * p1, k2, yo, k5, k2tog, p1*
R7 | * p1, k3, yo, k4, k2tog,p1*
R9 | * p1, k4, yo, k3, k2tog, p1*
R11 | * p1, k5, yo, k2, k2tog, p1*
R13 | * p1, k6, yo, k1, k2tog, p1*
R15 | * p1, k7, yo, k2tog, p1*
R17 | * p1, slkpsso, k7, yo, p1*
R19 | * p1, slkpsso, k6, yo, k1, p1*
R21 | * p1, slkpsso, k5, yo, k2, p1*
R23 |* p1, slkpsso, k4, yo, k3, p1*
R25 | * p1, slkpsso, k3, yo, k4, p1*
R27 | * p1, slkpsso, k2, yo, k5, p1*
R29 | * p1, slkpsso, k1, yo, k6, p1*
R31 | * p1, slkpsso, yo, k7, p1*
