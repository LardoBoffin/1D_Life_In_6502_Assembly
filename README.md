# 1D Life In 6502 Assembly for the BBC Micro
An implementation of Life in 1D in 6502 Assembly for the BBC Micro, based on BASIC from Nakazoto (thanks Nakazoto for the video and BASIC, it has reignited by retro programming enthusiasm) - see https://github.com/Nakazoto/CenturionComputer/blob/main/Software/New%20Software/1DLIFE.BAS

This code was written to use the BBC BASIC built in assembler so you load the code in and type RUN. This assembles the machine code and then runs it. 

This is my first foray into the world of 6502 in many years and far and away the largest program I have written on 6502. I have read numerous books and watched quite a few videos so figured it was high time I actually did something. The video by Nakazoto was perfect as it explained the algorithm for 1D Life as well as giving a BASIC version to test against. The project was small enough for me to actually be able to finish in a couple of weeks of the odd hour here and there.

The first version is somewhat lacking in optimisation beyond counting down from 78 to 0 rather than counting up.

The loop that goes through the cells to either side of the cell (I+2 to I-2, skipping I=I) being assessed is unrolled in order to make it easier to write. I did consider making it into a loop afterwards but given the complexity of having to skip I when it equals I (so that it does not count itself for the purposes of determining the number of neighbours) I didn't see that it would help much.

The easiest way to run this is to copy the contents of the code file into an emulator such as BeebEm (copy the 1DFile.6502 file contents, go to BeebEm, select Edit and then Paste) and then just type RUN.

To do:
1) Get rid of the flashing cursor
2) Optimise it a bit
3) Write a version that assembles from BeebAsm

Note that I got the random number generator by asking AI to produce a 6502 random number generator using the BBC Micro clock as the start point for the seed. So if you recognise the code I guess it looked at your repo to answer the question! In which case thanks and apologies for the plagiarism / lack of credit.
