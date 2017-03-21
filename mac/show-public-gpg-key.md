# Show public GPG key

After learning how to generate a gpg-key in Mac Os i had to find my public gpg-key to send it somebody.

It's easy as pie!

```bash
gpg --list-secret-keys --keyid-format LONG
```

This prints the following list:
```bash
/Users/hubot/.gnupg/secring.gpg
------------------------------------
sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10]
uid                          Hubot 
ssb   4096R/42B317FD4BA89E7A 2016-03-10
```

I just have to paste the GPG key ID i would like to use.
In this example, the GPG key ID is **3AA5C34371567BD2**.

```bash
gpg --armor --export 3AA5C34371567BD2
```

This will print out the public gpg-key beginning with `-----BEGIN PGP PUBLIC KEY BLOCK-----` and ending with `-----END PGP PUBLIC KEY BLOCK-----`. 