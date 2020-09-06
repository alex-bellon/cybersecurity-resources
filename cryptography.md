# Cryptography

## Articles
- Enigma
  - [AMS Article](http://www.ams.org/publicoutreach/feature-column/fcarc-enigma)
  - [Codes and Ciphers Book (Ch 9)](http://www.ik4hdq.net/codici_cifr.pdf)

## Blogs
- [BitsDeep](https://bitsdeep.com/)
- [Crypto for Social Good](https://cs.brown.edu/~seny/2950v/) - Class focused on the impact of crypto & privacy on marginalized groups

## Competitions
- [International Olympiad in Cryptography](https://nsucrypto.nsu.ru/)

## Books
- [Applied Cryptography](https://www.schneier.com/books/applied_cryptography/)
- [Cracking codes with Python](https://nostarch.com/crackingcodes)
- [Cryptography Engineering](https://www.schneier.com/books/cryptography_engineering/)
- [Serious Cryptography](https://nostarch.com/seriouscrypto)
- [The Code Book](https://en.wikipedia.org/wiki/The_Code_Book)
- [The Codebreakers](https://en.wikipedia.org/wiki/The_Codebreakers)
- [Crypto101](https://www.crypto101.io/)

## Concepts
- [A Crash Course in Everything Cryptographic](https://medium.com/@lduck11007/a-crash-course-in-everything-cryptographic-50daa0fda482)
- [A Guide to Post-Quantum Cryptography](https://hackernoon.com/a-guide-to-post-quantum-cryptography-d785a70ea04b)
- [Cryptographic Attacks](https://en.wikipedia.org/wiki/Category:Cryptographic_attacks)
- [Shor's Algorithm](https://www.scottaaronson.com/blog/?p=208)

### Ciphers
- [ADFGVX Cipher](https://crypto.interactive-maths.com/adfgvx-cipher.html) - it combines an adapted Polybius Square with Columnar Transposition
- [Beaufort Cipher](http://practicalcryptography.com/ciphers/beaufort-cipher/)
- [Pollux Cipher](https://www.dcode.fr/pollux-cipher)
- [Sarah2 Cipher](https://laser-calcium.glitch.me/) - Sarah2 is a cipher meant to be implemented by hand with only simple tools.
- [VIC Cipher](https://en.wikipedia.org/wiki/VIC_cipher)

### Diffie Hellman
- Encryption without padding is insecure
  - Encryption: SAEP, OAEP+
  - Signature: PSS
- Diffie Hellman relies on:
    - Discrete log problem
    - Computational DH problem
    - Decisional DH problem
  - Use this setting for public key crypto (Cramer-Shoup) or signatures (Schnorr, DSA). Mostly used for DH though.
  - Really for this setting you just need a group G = <G> of prime order q when DDH problem is hard
  - Can also get this structure from the group of points of an elliptic curve
    - Advantages
      - Much smaller parameters
      - Much more efficient operations
      - Picking parameters is easier and less error-prone
    - Modern protocols use
      - ECDH for key exchange
      - ECDSA, RSA (legacy) for signatures
Mod p, every invertible element has order dividing p-1 (with operation multiplication)

### RSA
#### keyGen
- pick primes p, q
- set N = pq
- set e = 65537
- compute d s.t. e * d ≡ 1 mod (p - 1)(q - 1)

#### RSA function
f: (**Z**/N**Z**)<sup>x</sup> -> (**Z**/N**Z**)<sup>x</sup>

f: x -> x<sup>e</sup> mod N

f<sup>-1</sup>: y -> y<sup>d</sup> mod N

#### Hard problems
**Factoring**: given N, find p and q

**RSA problem**: given N, e, y, find x s.t.x<sup>e</sup> = y

#### Signatures from RSA
**KeyGen**: pubkey = (N, e), seckey = d

**Sign M**: σ = [Pack(M)]<sup>d</sup> mod N, Pack in (**Z**/N**Z**)<sup>x</sup>

**Verify**: σ<sup>e</sup> ≡ Pack(M) mod N

#### Encryption from RSA
k <- AE keyspace<br>
c = E Pack(k)<sup>e</sup> mod N

**Decrypt**: E Unpack(c<sup>d</sup> mod N) to get x

## Learning
- [A Graduate Course in Applied Cryptography](https://toc.cryptobook.us/) - Full textbook online
- [Dan Boneh](https://crypto.stanford.edu/~dabo/) - Crypto prof at Stanford, has a lot of good resources (including a textbook!)
- [The Amazing King](http://theamazingking.com/crypto.php)
- [An Introduction to Mathematical Cryptography](https://www.math.brown.edu/~jhs/MathCryptoHome.html)
- [Lessons learned and misconceptions regarding encryption and crypto](https://security.stackexchange.com/questions/2202/lessons-learned-and-misconceptions-regarding-encryption-and-cryptology/2206#2206)
- [An Intensive Introduction to Cryptography](https://intensecrypto.org/public/)
- [Practical Crypto](https://github.com/matthewdgreen/practicalcrypto) - Repository for course materials and slides for Practical Cryptographic Systems, JHU CS 445/645.
- [Advanced Crypto Notes](https://cs.nyu.edu/courses/fall09/G22.3220-001/index.html) - Notes from NYU
- [Advanced Topics in Cryptography](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-876j-advanced-topics-in-cryptography-spring-2003/lecture-notes/) - MIT OCW course
- [Cryptography Notes](https://people.eecs.berkeley.edu/~luca/cs276/#notes) - Notes from UC Berkeley
- [Intro to Cryptography Notes](https://www.cs.umd.edu/~jkatz/gradcrypto2/scribes.html) - Notes from NYU
- [Intro to Cryptography Notes](https://sites.fas.harvard.edu/~cs120/lectures/) - Notes from Harvard
- [Lecture Notes on Cryptography](https://cseweb.ucsd.edu/~mihir/papers/gb.pdf) - Cryptography Notes by Shafi Goldwasser
- [Scribed Lecture Notes](https://www.cs.umd.edu/~jkatz/gradcrypto2/scribes.html) - Lecture notes from Grad Crypto at University of Maryland
- [Lattices in Computer Science](https://cims.nyu.edu/~regev/teaching/lattices_fall_2009/index.html) - Lattice based cryptography notes from NYU
- [Lattice Based Cryptography and Applications](https://cyber.biu.ac.il/event/the-2nd-biu-winter-school/) - Lattice crypto notes from BIU
- [Lattice Based Cryptography and Applications](https://cyber.biu.ac.il/event/the-2nd-biu-winter-school/) - Lattice crypto notes from BIU
- [Advanced Topics in Cryptography: Lattices](https://people.csail.mit.edu/vinodv/6876-Fall2015/index.html) - notes from MIT
- [Lightweight Introduction to Lattices](https://www.cryptool.org/images/ctp/documents/Lattice-Introduction_v015.pdf)
- [An Intensive Introduction to Cryptography](https://intensecrypto.org/public/)

## Papers
- [The Moral Character of Cryptographic Work](https://web.cs.ucdavis.edu/~rogaway/papers/moral-fn.pdf)

## Practice
- [Cryptopals](https://cryptopals.com/)
- [ToadStyle Cryptopals](https://toadstyle.org/cryptopals/)
- [CryptoHack](https://cryptohack.org/challenges/)
  - [CryptoHack Docker](https://github.com/hyperreality/cryptohack-docker)

## Reddit
- [Does a one time pad expose itself as a one time pad?](https://www.reddit.com/r/crypto/comments/bcytd6/does_a_one_time_pad_expose_itself_as_a_one_time/s)
- [How are repeated IVs used to crack the key?](https://www.reddit.com/r/crypto/comments/brdgnl/how_are_repeated_ivs_used_to_crack_the_key/)
- [Nonce reuse vs IV reuse](https://www.reddit.com/r/crypto/comments/fnku50/nonce_reuse_vs_iv_reuse/)

## Tools
- [AntiMersenne](https://github.com/nh2/AntiMersenne) - Predicting Python's Mersenne twister PRNG for 30c3 CTF, with Python calling Java
- [Ciphey](https://github.com/Ciphey/Ciphey) - Automatically decode encryptions without a key, decode encodings, and crack hashes 
- [cribdrag](https://github.com/SpiderLabs/cribdrag) - an interactive crib dragging tool for cryptanalysis on ciphertext generated with reused or predictable stream cipher keys
- [Crib Dragging Auto Cracker](https://github.com/yhuag/Crib-Dragging-Auto-Cracker) - The project is to crack crib dragging in an efficient way. It will crib drag 5,000 most common English vocabularies on the cipher text and collect all the words that are partially/entirely recognized as an English word.
- [crypto_misc](https://github.com/elliptic-shiho/crypto_misc) - Paper Implementation, Practice code, Cryptographic some others.
- [cryptobin](https://github.com/avanpo/cryptobin) - crypto and puzzle tools
- [Crypton](https://github.com/ashutosh1206/Crypton) -  Library consisting of explanation and implementation of all the existing attacks on various Encryption Systems, Digital Signatures, Key Exchange, Authentication methods along with example challenges from CTFs
- [Cryptool](https://www.cryptool.org/en/cryptool-online)
- [CryptoTools](https://cryptotools.net/) - a suite of cryptographic utilities for convenience that operate entirely on the client side. No calculations take place on the server, nor is any data generated or used here sent to the server.
- [Cryptoprograms](http://www.cryptoprograms.com/) - Make and decrypt ciphers
- [Decodify](https://github.com/s0md3v/Decodify) - It can detect and decode encoded strings, recursively.
- [hashID](https://github.com/psypanda/hashID) - Identify the different types of hashes used to encrypt data and especially passwords.
- [Mersenne Twister Predictor](https://github.com/kmyk/mersenne-twister-predictor) - Predict MT19937 PRNG, from preceding 624 generated numbers. There is a specialization for the "random" of Python standard library.
- [Outguess](https://web.archive.org/web/20150419030527/http://www.outguess.org/)
- [RC4-40-brute-office](https://github.com/kholia/RC4-40-brute-office) - Guaranteed cracking of M$ Office files using RC4 40-bit encryption
- [RC4 Python](https://github.com/g2jun/RC4-Python) - A simple encrypt/decrypt Python script using RC4
- [Replicated Random](https://github.com/fta2012/ReplicatedRandom)
- [RSA CTF Tool](https://github.com/Ganapati/RsaCtfTool) - RSA attack tool (mainly for ctf) - retreive private key from weak public key and/or uncipher data
- [rsa-stream](https://github.com/substack/rsa-stream) - encrypt/decrypt rsa with streams
- [XOR Analyze](https://github.com/ThomasHabets/xor-analyze) - Program for cryptanalyzing xor "encryption" with variable key length
