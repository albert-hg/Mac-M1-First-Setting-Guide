# Mac-M1-First-Setting-Guide

## Recommended Apps in App Store

1. [Magnet](https://apps.apple.com/tw/app/magnet/id441258766?mt=12)


## Terminal Setting

1. [Bash prompt setting](https://osxdaily.com/2006/12/11/how-to-customize-your-terminal-prompt/)

        albert@MyMac ~ % echo $PS1      // %n@%m %1~ %#
        albert@MyMac ~ % export PS1="%n#"
        albert#


## Homebrew

Homebrew is a tool for managing those applications on your mac. It has supported on Mac M1, but it will have different installation path base on the chips:

* macOS Intel:      /usr/local
* Apple Silicon:    /opt/homebrew

In installation, you can install Homebrew by *bash* or *zsh*, and [the different](https://www.educba.com/zsh-vs-bash/) in the between is about the *Configuration file*.


> The configuration files are .bashrc in non-login interactive shells and .profile or .bash_profile in login shells of Bash. 
> 
> In Zsh, non-login shells are .zshrc and login shells are .zprofile.



### [Install Steps (M1)](https://docs.brew.sh/Installation)

1. Open your *terminal.app*
1. Install Homebrew in one line by *bash* or *zsh* (here use *bash*)

        # /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

1. Set Homebrew into the *PATH*

        # echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
        # eval "$(/opt/homebrew/bin/brew shellenv)"
        # brew help
