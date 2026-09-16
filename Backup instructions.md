```bash
gpg --keyserver hkps://keys.openpgp.org --recv-keys 48489624F69EAF4A
```

or 
```bash
# Fetch the public key from your Forgejo server
curl -O https://forge.ucalgarybaja.ca/darkicewolf50/.profile/raw/branch/master/yubikey-public.gpg

curl -O https://forge.ucalgarybaja.ca/darkicewolf50.gpg

# Import into GPG
gpg --import yubikey-public.gpg

gpg --import darkicewolf50.gpg
```

```bash
gpg --card-status
```

```bash
git config --global user.signingkey 48489624F69EAF4A
git config --global commit.gpgsign true
```

# SSH Key

```bash
ssh-keygen -K
```

```bash
nano ~/.ssh/config
```

```sshconfig
Host *
    IdentityFile ~/.ssh/id_ed25519_yubikey
    IdentitiesOnly yes
```