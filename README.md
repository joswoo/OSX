# OSX(High Sierra)

## Install Xcode
- After Install
> $ sudo xcodebuild -license
> $ sudo xcode-select --install

## Homebrew
- Install
> $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
> $ brew update
> $ vi ~/.bash_profile
Add this below code
```
# Homebrew
export PATH=/usr/local/bin:$PATH
```
> $ source ~/.bash_profile

- Uninstall
> $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"

- Remove all installed packages
> $ brew remove --force $(brew list) --ignore-dependencies
> $ brew cleanup

## Install Python
> $ brew install python
> $ brew linkapps python
