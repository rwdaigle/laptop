How to setup my laptop.

## Settings

1. Update computer name in Sharing settings
2. Turn on FileVault, Firewall in Security settings
3. Move dock

## Apps

```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
brew install caskroom/cask/brew-cask wget mackup docker heroku-toolbelt git rbenv ruby-build pow
brew tap homebrew/dupes ; brew install apple-gcc42
brew install --HEAD docker-machine
brew cask install google-chrome 1password dropbox atom sonos slack todoist bartender divvy stay bettertouchtool alfred ynab mailplane licecap vmware-fusion
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
sudo rm -rf Public Documents
ln -s ~/Dropbox\ \(Personal\) Dropbox
ln -s ~/Dropbox/Personal/System/bin bin
ln -s ~/Dropbox/Personal/Documents .
mackup restore
```

## Code

```shell
mkdir ~/dev ~/dev/spreedly
cd ~/dev/spreedly
for i in "core" "id" "cryptoad" "docs" "bootstrap"; do
  git clone https://github.com/spreedly/$i.git
done
```

Then follow Spreedly dev setup instructions...
