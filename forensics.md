# Forensics

## Concepts
- [Hiding text in pixels](http://www.msarnoff.org/millitext/)
- [SSTV](https://en.wikipedia.org/wiki/Slow-scan_television)
 - [Example challenge writeup](https://github.com/Dvd848/CTFs/blob/master/2019_picoCTF/m00nwalk.md)
- [Zero width characters](https://www.zachaysan.com/writing/2017-12-30-zero-width-characters)
- [Zip files all the way down](https://research.swtch.com/zip)

### Countdown
- https://incoherency.co.uk/countdown/
  - [Solver](https://github.com/jes/cntdn) - Solvers for the countdown letter and number games.

### File Headers
- [File Header Cheatsheet](https://digital-forensics.sans.org/media/hex_file_and_regex_cheat_sheet.pdf)

### GIFAR
- [GIFAR Linux Version](https://www.howtogeek.com/270668/how-to-hide-a-file-or-folder-in-an-image-in-linux/)
- [GIFAR Wikipedia](https://en.wikipedia.org/wiki/Gifar)
- [GIFAR Windows Version](https://www.howtogeek.com/119365/how-to-hide-zip-files-inside-a-picture-without-any-extra-software/)

[Walkthrough](https://quadhead.de/storing-javascript-code-in-gif-images/)

### Mojibake
- https://incoherency.co.uk/mojibake/

## Tools

### General
- https://georgeom.net/StegOnline/checklist
- [Autopsy](http://www.sleuthkit.org/autopsy/download.php) - Digital forensics platform
- [bulk_extractor](https://github.com/simsong/bulk_extractor) - Scans a disk image, a file, or a directory of files
- [dc3dd](https://sourceforge.net/projects/dc3dd/) - A patched version of GNU dd with added features for computer forensics
- [DumpsterDiver](https://github.com/securing/DumpsterDiver) - Analyze big volumes of various file types in search of hardcoded secrets
- [Entropy](https://github.com/lsauer/entropy) - ent is a small, fast command line utility, plotting various entropy related metrics of files or pipe/stdin streams 
- [ExifTool](https://github.com/exiftool/exiftool) - Read, Write and Edit Exif metadata
- [Foremost](https://linux.die.net/man/1/foremost) - Restore files from their headers, footers and data structures
- [frida-extract](https://github.com/OALabs/frida-extract) - Based RunPE extraction tool
- [Kaitai](https://ide.kaitai.io/) - Reverse engineer different formats of files
- [PdfParser](https://github.com/smalot/pdfparser) - A standalone PHP library, provides various tools to extract data from a PDF file
- [peepdf](https://github.com/jesparza/peepdf) - Powerful Python tool to analyze PDF documents
- [scalpel](https://github.com/sleuthkit/scalpel) - Scalpel is an open source data carving tool.
- [SSTV decoder](https://github.com/colaclanth/sstv)
- [volatility](https://github.com/volatilityfoundation/volatility) - Volatile memory extraction utility framework
- [whatsapp-viewer](https://github.com/andreas-mausch/whatsapp-viewer) - Small tool to display chats from the Android msgstore.db database
- [zwfp](https://github.com/vedhavyas/zwfp) - Zero-Width fingerprinting

### Passwords
- [BEWGor](https://github.com/berzerk0/BEWGor) - Bull's Eye Wordlist Generator
- [bruteforce-wallet](https://github.com/glv2/bruteforce-wallet) - Try to find the password of an encrypted Peercoin (or Bitcoin, Litecoin, etc...) wallet file
- [chntpw](http://pogostick.net/~pnh/ntpasswd/) - Utility to reset the password on Windows
- [chromepass](https://www.nirsoft.net/utils/chromepass.html) - View passwords stored by Google Chrome Web browser
- [crowbar](https://github.com/galkan/crowbar) - Brute forcing tool
- [cupp](https://github.com/Mebus/cupp) - Common User Passwords Profiler
- [hashcat](https://hashcat.net/hashcat/) - Advanced Password Recovery
  - [Hob0Rules](https://github.com/praetorian-code/Hob0Rules) - Password cracking rules for Hashcat based on statistics and industry patterns
- [John the Ripper](https://www.openwall.com/john/) - A fast password cracker
 - [John tutorial](https://charlesreid1.com/wiki/John_the_Ripper/Password_Generation)
 - [Another John tutorial](https://blog.sleeplessbeastie.eu/2015/05/25/how-to-crack-archive-password-faster/)
- [KON-BOOT](https://www.piotrbania.com/all/kon-boot/) - Wim/Mac password breaker
- [LaZagne](https://github.com/AlessandroZ/LaZagne) - Credentials recovery project
- [mimikatz](https://github.com/gentilkiwi/mimikatz) - A little tool to play with Windows security
- [passwordfox](https://www.nirsoft.net/utils/passwordfox.html) - Extract the user names/passwords stored in Firefox
- [RarCrack](http://rarcrack.sourceforge.net) - Crack .rar passwords
- [SSH-Brute-Forcer](https://github.com/R4stl1n/SSH-Brute-Forcer) - A Simple Multi-Threaded SSH Brute Forcer
- [thc-hydra](https://github.com/vanhauser-thc/thc-hydra) - Parallelized login cracker which supports numerous protocols to attack
- [WCE](https://www.ampliasecurity.com/research/windows-credentials-editor/) - Windows Credentials Editor

### Printing
- [Print Watch](http://www.prnwatch.com/ok-printer-viewer/) - See what people printed

### Steganography
- https://0xrick.github.io/lists/stego/
- [Chess Steganography](https://github.com/jes/chess-steg)
- [spectrology](https://github.com/solusipse/spectrology) - Images to audio files with corresponding spectrograms encoder.
- [Stego Toolkit](https://github.com/DominicBreuker/stego-toolkit) - Collection of steganography tools - helps with CTF challenges
