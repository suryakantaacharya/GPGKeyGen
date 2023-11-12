# GPGKeyGen

- Sample terminal commands to do GPG key gen


gpg --full-generate-key
gpg (GnuPG) 2.2.40; Copyright (C) 2022 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 
Requested keysize is 3072 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 
Key does not expire at all
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Suryakanta Acharya
Email address: *************@*****.com
Comment: 
You selected this USER-ID:
    "Suryakanta Acharya <*************@*****.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? 
Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: directory '/home/surya/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/home/surya/.gnupg/openpgp-revocs.d/****************************.rev'
public and secret key created and signed.

pub   rsa3072 2023-11-12 [SC]
      E1AD2186E6062497C9CEE9AAB1EF7BB2F2FF5C5D
uid                      Suryakanta Acharya <*************@*****.com>
sub   rsa3072 2023-11-12 [E]

surya@suryas-pc:~$ gpg --list-keys
gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
/home/surya/.gnupg/pubring.kbx
------------------------------
pub   rsa3072 2023-11-12 [SC]
      E1AD2186E6062497C9CEE9AAB1EF7BB2F2FF5C5D
uid           [ultimate] Suryakanta Acharya <*************@*****.com>
sub   rsa3072 2023-11-12 [E]

surya@suryas-pc:~$ gpg --armor --export  rsa3072 > public_key.asc
gpg: WARNING: nothing exported
surya@suryas-pc:~$ gpg --armor --export  3072 > public_key.asc
gpg: WARNING: nothing exported
surya@suryas-pc:~$ gpg --armor --export  **************************** > public_key.asc
surya@suryas-pc:~$ gpg --export-secret-keys --armor **************************** > secret_key.asc
surya@suryas-pc:~$ 

