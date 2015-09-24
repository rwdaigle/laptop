How to setup my laptop.

## Settings

1. Update computer name in Sharing settings
2. Turn on FileVault, Firewall in Security settings
3. Move dock

## Apps

```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install caskroom/cask/brew-cask wget mackup
brew cask install google-chrome 1password dropbox atom sonos slack todoist bartender divvy stay bettertouchtool alfred ynab mailplane licecap
```

Then open and login to (in order)
  * Dropbox
  * 1Password

Manually install the following from the App Store

* Gifwit
* Cloudapp

## Configuration

Once Dropbox is done syncing, link everything up and restore configuration:

```shell
sudo rm -rf Movies Music Pictures Public Documents
ln -s ~/Dropbox\ \(Personal\) Dropbox
ln -s ~/Dropbox/Personal/System/bin bin
ln -s ~/Dropbox/Personal/Documents .
mackup restore
```

