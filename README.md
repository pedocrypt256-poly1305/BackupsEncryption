# BackupsEncryption
Anything related to things that need to be secured with my password, while having redundancy.

1. 2025TS.kbdx This is my main password manager file. It uses my password and keyfile.
2. VCRescueDisk.zip is my disk encryption header key backup. Its hash is stored in 2025TS.kbdx.
3. KFileForKPass.kdbx stores my keyfile (in attachments) required to mount 2025TS.kbdx. It uses the same disk encryption password
   as VCRescueDisk.zip.

2025TS.kbdx and KFileForKPass.kbdx uses Twofish algorithm.

Configurations:
2025TS.kbdx uses Twofish algorithm, AES-KDF=1
VCRescueDisk.zip's algorithm, hash, and PIM is classified.
KFileForKPass.kbdx uses Twofish algorithm, Argon2d with rounds=17, memory=8192 Mib, and 8 threads parallelism.

All "passwords" exceed 25 characters (160 bit entropy).
There's TRNG data mixed into my passwords to resist dictionary attacks.
