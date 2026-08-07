# 1D Life In 6502 Assembly for the BBC Micro
An implementation of Life in 1D in 6502 Assembly for the BBC Micro, based on BASIC from Nakazoto (thanks Nakazoto for the video and BASIC, it has reignited by retro programming enthusiasm) - see https://github.com/Nakazoto/CenturionComputer/blob/main/Software/New%20Software/1DLIFE.BAS

This code was written to use the BBC BASIC built in assembler so you load the code in and type RUN. This assembles the machine code and then runs it.

The first version is somewhat lacking in optimisation beyond counting down from 78 to 0 rather than counting up.

The loop that goes through the cells to either side of the cell (I+2 to I-2, skipping I=I) being assessed is unrolled in order to make it easier to write. I did consider making it into a loop afterwards but given the complexity of having to skip I when it equals I (so that it does not count itself for the purposes of determining the number of neighbours) I didn't see that it would help much.
