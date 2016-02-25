How to setup my laptop.

## Settings

1. Update computer name in Sharing settings
2. Turn on FileVault, Firewall in Security settings
3. Move dock

## Apps

```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
brew install caskroom/cask/brew-cask wget mackup docker heroku-toolbelt git rbenv ruby-build pow homebrew/versions/erlang-r17 gpg ngrok hub
brew tap homebrew/dupes ; brew install apple-gcc42
brew install --HEAD docker-machine
wget https://github.com/elixir-lang/elixir/releases/download/v1.0.5/Precompiled.zip
unzip Precompiled.zip -d ~/bin/elixir-1.0
brew cask install dropbox slack todoist bartender divvy stay bettertouchtool alfred ynab mailplane licecap vmware-fusion viscosity fluid
```

Manually install the following from the App Store

* 1Password
* IA Writer
* Gifwit
* Monosnap
* Sonos

Manually install:

* [Atom](https://atom.io)
* [Chrome](https://www.google.com/chrome/browser/desktop/)

Then open and login to (in order)

* Dropbox
* 1Password

## Configuration

Once Dropbox is done syncing, link everything up and restore configuration:

```shell
sudo rm -rf Public Documents
ln -s ~/Dropbox\ \(Personal\) Dropbox
ln -s ~/Dropbox/Documents .
mackup restore
```

Then manually:

* Setup Fluid app to `https://calendar.google.com/calendar/render`

## Code

```shell
mkdir ~/dev ~/dev/spreedly
cd ~/dev/spreedly
for i in "core" "id" "cryptoad" "docs" "bootstrap" "internal-docs"; do
  git clone https://github.com/spreedly/$i.git
done
```

Then follow Spreedly dev setup instructions...
