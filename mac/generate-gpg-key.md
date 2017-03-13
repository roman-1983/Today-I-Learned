# How to generate a GPG Key in Mac Os

I saw that i can sign my Github commits with a gpg-key. But before doing this i had to learn how to generate a gpg-key in Mac Os.

First i had to install `gpg` via [Homebrew](https://brew.sh).
```bash
brew install gpg
```

After that i can run `gpg`. This will fire up an interactive dialog which asks for the options to generate the gpg-key.
```bash
gpg --gen-key
```

The output will look like this:

```bash
Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   Your selection?
``` 

I want to generate `RSA and RSA`. So my choice is **1**. 

```bash
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (2048)
```

The key should be as safe as possible, so i will use **4096** bits.

```bash
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0)
```

The key should not expire, so i chose **0**.

```bash
Key does not expire at all
Is this correct? (y/N)
```

**Y**es, i am sure! ;-)

```bash
GnuPG needs to construct a user ID to identify your key.

Real name: Firstname Lastname
Email address: your@mailadress.com
Comment:
```

Nearly finished, i just had to enter my personal information and confirm them.

After that a dialog for a passphrase will fire it twice.
```bash
                              ┌─────────────────────────────────────────────────────┐
                              │ Enter passphrase                                    │
                              │                                                     │
                              │                                                     │
                              │ Passphrase ********________________________________ │
                              │                                                     │
                              │       <OK>                             <Cancel>     │
                              └─────────────────────────────────────────────────────┘
```

That's it - i have successfully generated a gpg-key!

The key is saved in `~/.gnupg`