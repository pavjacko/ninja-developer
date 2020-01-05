# Setup

Recommended full setup for your macOS development environment

I use this setup to develop cross-platform apps

# General 

## Install iTerm

https://www.iterm2.com/downloads.html

## Install zsh

```bash
brew install zsh
```

## Setup bash_profiles


in your `~./zshrc` add

```
export PATH=/usr/local/bin:$PATH

source ~/.bash_profile

export NVM_DIR="$HOME/.nvm"
. "$HOME/.nvm/nvm.sh"

[[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm"

[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  
```

## Setup Git

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
eval "$(ssh-agent -s)"
ssh-add -K ~/.ssh/id_rsa
pbcopy < ~/.ssh/id_rsa.pub
```

Fort Github: Add copied ssh to your settings.
https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account

## Install `rvm`

https://rvm.io/rvm/install

```bash
brew install gnupg
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash
source ~/.rvm/scripts/rvm
```

or update rvm to latest
```bash
rvm get stable
```

## Install `ruby`

```bash
rvm install ruby --latest
rvm use ruby --latest
```

## Install `nvm`

https://github.com/nvm-sh/nvm

```bash
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
source ~/.bashrc
```
If you already have nvm, update to latest:

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```

## Install `nodejs`

```bash
nvm install node
nvm use node
nvm alias default node
export NODE_OPTIONS="--max_old_space_size=8192" # Decrease/Increase depending on your RAM preferences
```

## Install `npx`

```bash
npm install -g npx
```

## Install JDK 1.8

There are several issues with new versions of JDK. 1.8 works the best. 

Since 05/2019 Oracle started being (bigger than usual) di*ks about the JDK downloads and you have to use their website and register to get older versions:

https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

# iOS, Mac Development 

## Install Cocoapods

```bash
sudo gem install cocoapods
```

## Install Xcode Tools

```bash
xcode-select --install
```

## Install Fastlane


```bash
sudo gem install fastlane -NV
```

## Install `iOS` Tools

Install latest XCode from App Store and start it once to accept license and install extra stuff

## Apple ID with Developer Program

You need to have signed in with an Apple ID which is part of the AppGyver's Apple Developer Program.

Link your Apple ID account to Xcode:

1. Open Xcode
1. Open _Preferences_ from the Xcode menu
1. Go to _Accounts_ tab
1. Click + to add a new _Apple ID_
1. Enter your Apple ID login credentials

# Android Development 

## Install `Android` Tools

Install latest Android Studio https://developer.android.com/studio/ and launch it.

You need to install NDK from the SDK manager:

1. Create new project with defaults suggested by studio and open it
1. Let it settle
1. Open _Tools_ -> _SDK manager_
1. Open _SDK Tools_ tab
1. Check _NDK_
1. Click OK and proceed with the install


Restart your computer here to let Android SDK related environment variables spread to your terminal. (sourcing, restarting bash or restarting Terminal.app was not enough on a clean machine)

# TV Development 

## Install Oracle VM

```bash
brew cask install virtualbox
```

## Install Tizen SDK

https://developer.tizen.org/development/tizen-studio/download


## Install LG WebOS SDK

http://webostv.developer.lge.com/sdk/installation/