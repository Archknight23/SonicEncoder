# SonicEncoder - Musical Encryption, or "How to take your target's data sexily and with the power of EDM." 
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
