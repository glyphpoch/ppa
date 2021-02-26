# Simple Ubuntu PPA

Contains software that hasn't made it into the official Ubuntu repo yet...

# Adding new packages

Add the new package into the repository directory. It can be in the root directory or in any sub-folder structure.

Run the following to generate `Packages` and `*Release*` files:
```sh
EMAIL=your-email-here@domain.ext ./add-packages.sh
```

A valid GPG key must be set up for the above command to work.

# Using the PPA:
```
curl -s --compressed "https://glyphpoch.github.io/ppa/KEY.gpg" | sudo apt-key add -
sudo curl -s --compressed -o /etc/apt/sources.list.d/glyphpoch_ppa.list "https://glyphpoch.github.io/ppa/glyphpoch_ppa.list"
sudo apt update
```

# References:
* <https://assafmo.github.io/2019/05/02/ppa-repo-hosted-on-github.html>
