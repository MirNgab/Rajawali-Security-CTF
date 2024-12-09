# Kelinci percobaan - 10 Points
> My name is Rabbit U2FsdGVkX199giUiA0anSkkyYQdZEBboqStIAIbz60JFiEZbspGONiX7tLrvXilk
### Solution
The way the name of the challenge and the description saying the word rabbit, i jump to the conclusion that this is Rabbit Encryption

> Rabbit uses a 128-bit key and a 64-bit initialization vector. The cipher was designed with high performance in software in mind, where fully optimized implementations achieve an encryption cost of up to 3.7 cpb on a Pentium 3, and of 9.7 cpb on an ARM7. However, the cipher also turns out to be very fast and compact in hardware.

The core component of the cipher is a bitstream generator which encrypts 128 message bits per iteration. The cipher's strength rests on a strong mixing of its inner state between two consecutive iterations. The mixing function is entirely based on arithmetical operations that are available on a modern processor, i.e., no S-boxes or lookup tables are required to implement the cipher. The mixing function uses a g-function based on arithmetical squaring, and the ARX operations – logical XOR, bit-wise rotation with fixed rotation amounts, and addition modulo 232.

The g-function used in Rabbit – squaring a 32-bit number to produce a 64-bit number, and then combining the left half and the right half of that square number with xor, to produce a 32-bit result – provides much better results than using the 32 middle bits of that squared number (the middle-square method).[5]
