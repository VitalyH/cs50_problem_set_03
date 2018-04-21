# cs50_problem_set_03

Specification
bday.txt
In bday.txt, type the ASCII representation of Happy Birthday, translating its sheet music, above, to the machine-readable representation prescribed herein. You should find that the song begins with:

D4@1/8
D4@1/8
E4@1/4
D4@1/4
G4@1/4
F#4@1/2
helpers.c
is_rest
Complete the implementation of is_rest in helpers.c. Recall that blank lines represent rests in our machine-readable format. And recall that synthesize will call this function in order to determine if one of the lines a user has typed in is indeed blank.

What does it mean for a line to be blank? To answer that question, start by looking at cs50.h itself, wherein get_string is documented:

https://github.com/cs50/libcs50/blob/develop/src/cs50.h

What do the comments atop get_string say that the function returns if a user simply hits Enter, thereby inputting only a "line ending" (i.e., \n)?

When is_rest is subsequently passed such a string, s, how should it (nay, you!) recognize as much?

duration
Complete the implementation of duration in helpers.c. Recall that this function should take as input as a string a fraction and convert it into some integral number of eighths. You may assume that duration will only be passed a string formatted as X/Y, whereby each of X and Y is a positive decimal digit, and Y is, moreover, a power of 2.

frequency
Finally, complete the implementation of frequency in helpers.c. Recall that this function should take as input as a string a note (e.g., A4) and return its corresponding frequency in hertz as an int.

And recall that:

The frequency, f, of some note is 2n/12 × 440, where n is the number of semitones from that note to A4.

Each key on a piano is said to be one semitone, otherwise known as a half step, away from its adjacent neighbor, whether white or black.

The effect of # and b, otherwise known as accidentals, is to raise or lower, respectively, the pitch of a note by one semitone.

In implementing this function, you might find pow and round, both declared in math.h, of interest.
