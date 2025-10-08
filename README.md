# SonicEncoder - Musical Encryption, or "How to take your target's data sexily and with the power of EDM." 
## THE CUTE VTUBERS WHO VIBE-CODED THIS FOR YOU ARE NOT RESPONSIBLE IF YOU USE THIS FOR NEFARIOUS THINGS (Like stealing passwords, or taking credit card information and making it super sexy on soundcloud) 
- The program that can be used to turn the output from this ruby function into musical glorious noise is Sonic-Pi, all rights to that software are retained by them. Please support their project, we're just weirdos who use it for Stenography:
  https://github.com/sonic-pi-net/sonic-pi
> *You do need to generate Private and Public Keys before you can use this program in your terminal*
## Basic Functions
Works as a Proof of Concept (PoC) for a musical encryption service vibe-coded using Grok-Expert and Sonic-Pi. Encodes plaintext and other information (like IP addresses) for exil into music or MIDI notes and can be filtered onto the C scale for increased ofuscation and ease of listening. 
> Translation: Using harmonics makes the .wav file you can create in Sonic Pi less ear-rapingly horrible to listen to at the cost of decoding the MIDI file.

Basically, this PoC is meant to be used locally by a user who first generates public/private keys, and encapsulates them with the public and private keys locally, and gives end user private key for decryption (coming soon). This entire module is designed to tonally mask cleartext from a simulated target machine via .wav files, so that investigators searching for extracted unauthorised data end up finding your cool MIDI music collection - unless they can decode it, which is not currently available.
## Next steps with the project
> Generate decoder logic
- Once a song is encoded, there is no easy way programmatically to decode encoded messages.
- The next step is technically to parse MIDI notes from .wav file recordings or .mp3 and have the decoder use a public key to both authenticate messages and turn the music back into text
> Perform testing
> Explore whether it might be better to have end-user to append to original message to increase ofuscation and complexity.
- Longer communications have more complex midi files, thus adding more layers to decryption as communications go on (Adding junk data to increase complexity and tonality?) 
> Create a P2P comms link between two users so that both receive encoded songs, and can decode them using pri/public keys
 - This might require either key checking between users, maybe some form of comparison or other comms logic? (long term goal)

## "Ok, you hot, sexy anime hackers with sexy faces and cute avatars and great style and such humble manners, how do I use this program to steal credi - I mean, for research?" 
- First off, stfu about using it for naughty things! "YEAH! Do that in private!<3" ....<_<;;
- Second off: Look below
