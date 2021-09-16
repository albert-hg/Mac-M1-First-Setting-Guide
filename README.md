# Mac-M1-First-Setting-Guide

- [Recommended Apps in App Store](#recommended-apps-in-app-store)
- [Terminal Setting](#terminal-setting)
- [Homebrew](#homebrew)
    - [Homebrew-Cask](#homebrew-cask-homebrew)
        - [iTerm2](#iterm2-cask)

## Recommended Apps in App Store

1. [Magnet](https://apps.apple.com/tw/app/magnet/id441258766?mt=12)

## Is Apple Silicon ready?

You can check the app which has prepared already in Apple Silicon in the following URL:

https://isapplesiliconready.com/

## Terminal Setting

1. [Bash prompt setting](https://osxdaily.com/2006/12/11/how-to-customize-your-terminal-prompt/)

        albert@MyMac ~ % echo $PS1      // %n@%m %1~ %#
        albert@MyMac ~ % export PS1="%n#"
        albert#


## [Homebrew](https://docs.brew.sh/)

Homebrew is a tool for managing those applications on your mac. It has supported on Mac M1, but it will have different installation path base on the chips:

* macOS Intel:      /usr/local
* Apple Silicon:    /opt/homebrew

In installation, you can install Homebrew by *bash* or *zsh*, and [the different](https://www.educba.com/zsh-vs-bash/) in the between is about the *Configuration file*.


> The configuration files are .bashrc in non-login interactive shells and .profile or .bash_profile in login shells of Bash. 
> 
> In Zsh, non-login shells are .zshrc and login shells are .zprofile.



Following those [Install Steps (M1)](https://docs.brew.sh/Installation) as below: 

1. Open your *terminal.app*
1. Install Homebrew in one line by *bash* or *zsh* (here use *bash*)

        # /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

1. Set Homebrew into the *PATH*

        # echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
        # eval "$(/opt/homebrew/bin/brew shellenv)"
        # brew help


## [Homebrew-Cask](https://github.com/Homebrew/homebrew-cask) (@Homebrew)

Homebrew Cask extends Homebrew, and it helps that you don't need to click, drag and drop while install some GUI applications.

    # brew install cask

Then it will install the *formulae*s as following:

    bdw-gc      gmp         libevent    m4          readline
    c-ares      gnutls      libffi      nettle      unbound
    cask        guile       libidn2     nghttp2     coreutils
    jansson     libtasn1    openssl@1.1 emacs       jemalloc
    libtool     p11-kit     gettext     libev       libunistring
    pkg-config


## [iTerm2](https://iterm2.com/) (@Cask)

iTerm2 is a replacement for Terminal. It brings the terminal into something modern features, eg. split panes, search hightlight, autocomplete, etc.

        # brew install --cask iterm2

After installed, you can get a configuration file *.zprofile* in *~/*, and also can see Item2 has installed in *Application* file already.
