# SonicEncoder

**[CFSD // RESEARCH ARTIFACT // X-106-05]**

> *"For legal reasons, Director, this writeup can't say it like THAT."*
> *"...Fine. Fine! 'Musical steganography,' happy now?"*
> — logged, Chaos Foundry Security Division

Steganography research proof-of-concept: encodes an RSA-encrypted payload as
MIDI notes and emits [Sonic Pi](https://github.com/sonic-pi-net/sonic-pi)
source that renders it as audio. The output is a short generative track —
readable as music, not as a payload — unless you hold the private key.

All rights to Sonic Pi are retained by its authors; support the project.

## How it works

1. `generatekeys.rb` — generates an RSA-2048 keypair (`private.pem` /
   `public.pem`).
2. `songitizer.rb` — takes a plaintext message (and optionally an IP:port),
   RSA-encrypts it against a recipient's public key, and maps the resulting
   bytes to MIDI note numbers.
3. Optional harmonic mode re-encodes each byte across the C major scale
   (base-7) instead of raw note range, trading a larger note sequence for
   audio that sounds intentional rather than random.
4. The script prints ready-to-run Sonic Pi source — drum-framed, reverbed —
   that renders the payload as a short generative track.

Decoding (MIDI/audio back to plaintext) is not implemented. That's the
open problem, not a withheld feature.

## Status

Proof of concept. No decoder yet, no P2P handshake, no obfuscation beyond
the harmonic mapping. Treat it as a demonstration that RSA ciphertext
survives a lossy round-trip through "notes a human would let play in the
background," not as a hardened channel.

## Roadmap

- Decoder: parse MIDI/WAV/MP3 back to ciphertext, authenticate and decrypt
  with the recipient's private key.
- Obfuscation: append junk data to lengthen and vary the note sequence.
- P2P exchange between two keyholders, with key verification.

## Scope

Research and educational use — steganographic encoding, key handling, and
the tradeoffs between payload size and how convincing the output audio is.
Not maintained as a covert-channel tool for use against systems you don't
own or have authorization to test.
