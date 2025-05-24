<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [My Mac Setup](#my-mac-setup)
  - [What Macbook do I haver?](#what-macbook-do-i-haver)
  - [OS Settings](#os-settings)
    - [Desktop](#desktop)
    - [Finder](#finder)
    - [Dock](#dock)
  - [Quick Launching](#quick-launching)
  - [Homebrew](#homebrew)
    - [Homebrew](#homebrew-1)
    - [RayCast Homebrew Plugin](#raycast-homebrew-plugin)
  - [Window Management](#window-management)
  - [App Switching](#app-switching)
  - [Menu Bar Utilities](#menu-bar-utilities)
    - [Hidden Bar](#hidden-bar)
  - [Web Browser](#web-browser)
    - [Brave Browser](#brave-browser)
  - [Other Apps I use](#other-apps-i-use)
  - [Other Apps I Use Daily](#other-apps-i-use-daily)
  - [Terminal](#terminal)
    - [Shell](#shell)
      - [Load dotfiles](#load-dotfiles)
    - [Github SSH Setup](#github-ssh-setup)
      - [Other command line tools I use](#other-command-line-tools-i-use)
  - [VS Code](#vs-code)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# My Mac Setup

This repo contains info of all the apps / tools / settings that I use in my daily life

---
## What Macbook do I haver?
I'm using two Apple Machines

1. MacBook Pro 2023 13"
    - Apple M2
    - 8 GB RAM
  

## OS Settings
  These are my preferred settings for Desktop, Finder and the Dock.

### Desktop
I don't use new Desktop, Stage Manager or Widget features in Sonoma, so I disable them.

* System Preferences
  * Desktop & Dock
    * Desktop & Stage Manager
      * Show Items
        * On Desktop -> uncheck
        * In Stage Manager -> uncheck
      * Click wallpaper to reveal desktop -> Only in Stage Manager
      * Stage Manager -> uncheck
      * Widgets
        * On Desktop -> uncheck
        * In Stage Manager -> uncheck

### Finder

* Finder -> Preferences
  * General -> Show these on the desktop -> Select None
      * I try to keep my desktop completely clean.
  * General -> New Finder windows show -> Home Folder
      * I prefer to see my home folder in each new finder window instead of recent documents
  * Advanced -> Show all filename extensions -> Yes
  * Advanced -> Show warning before changing an extension -> No
  * Advanced -> When performing a search -> Search the current folder
* View
  * Show Status Bar
  * Show Path Bar
  * Show Tab Bar

### Dock

I don't use the Dock at all. It takes up screen space, and I can use RayCast to launch apps and AltTab to switch between apps. I make the dock as small as possible and auto hide it.

* System Preferences
  * Desktop & Dock
    * Size -> Small as possible
    * Position on screen -> Left
    * Automatically hide and show the Dock -> Yes
    * Animate opening applications -> No
    * Show suggested and recent apps in the Dock -> No

## Quick Launching

The built in spotlight search is a bit slow for me and usually has web search results as the default instead of apps or folders on my machine.

I use  [RayCast](https://www.raycast.com/) as launcher.

```sh
brew install raycast
```
## Homebrew
### Homebrew

[Homebrew](https://brew.sh/) allows us to install tools and apps from the command line.

To install it, open up the built in `Terminal` app and run this command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This will also install the xcode build tools which is needed by many other developer tools.

After Homebrew is done installing, we will use it (via RayCast) to install everything else we need.


### RayCast Homebrew Plugin

Install the [RayCast Homebrew Plugin](https://www.raycast.com/nhojb/brew) so we can easily install formulae and casks directly from RayCast.

## Window Management

RayCast has this feature built in, but I use other app.

I use [rectangle](https://rectangleapp.com/) to move and resize windows using keyboard shortcuts. I used to use [spectacle](https://www.spectacleapp.com/), but rectangle is more regularly maintained and allows me to use all of the same keyboard shortcuts as spectacle.

I highly recommend installing this and memorizing the keyboard shortcuts. Fluid and seamless window management is key to being productive while coding.

Search for `rectangle` in RayCast `brew search` or:

```
brew install rectangle
```

## App Switching

The built in App switcher only shows application icons, and only shows 1 icon per app regardless of how many windows you have open in that app.

I use an app switcher called [AltTab](https://alt-tab-macos.netlify.app/). It shows full window previews, and has an option to show a preview for every open window in all applications (even minimized ones).

I replace the built-in `CMD+TAB` shortcut with AltTab.

Search for `alt-tab` in RayCast `brew search` or:

```sh
brew install alt-tab
```

## Menu Bar Utilities

### Hidden Bar

If you have several apps running that have menu bar icons, [Hidden Bar](https://github.com/dwarvesf/hidden) will let you choose which ones should be hidden after a timeout. This cleans things up if you have a ton of background apps running.

Search for `hiddenbar` in RayCast `brew search` or:

```sh
brew install hiddenbar
```

## Web Browser

### Brave Browser
 
 I used firefox just cause the privacy features built in.

 I use the following extensions to stay productive:

* [Tabliss](https://tabliss.io/) - simple new tab page
* [OneTab](https://www.one-tab.com/) - consolidate a bunch of open tabs into a shareable list of links
* [Dark Reader](https://darkreader.org/) - turn any site into dark mode (I'm not used to it yet)

## Other Apps I use 

## Other Apps I Use Daily
* [discord](https://discord.com/) - Messaging / Community
* [vlc](https://www.videolan.org/) - I use VLC to watch videos instead of the built in QuickTime.
* [keka](https://www.keka.io/en/) - Can extract 7z / rar and other types of archives
* [kap](https://getkap.co/) - Screen recorder / gif maker
* [figma](https://www.figma.com/) - Image editor
* [visual-studio-code](https://code.visualstudio.com/) - Code Editor
* [sublime-text](https://www.sublimetext.com/) - Note taking (I know there are better apps...)
* [docker](https://www.docker.com/products/docker-desktop/) - I don't need to explain this

You can install them in one go by placing them all into a text file and then running brew install:

```
discord
vlc
keka
kap
figma
visual-studio-code
sublime-text
insomnia
```

```sh
xargs brew install < apps.txt
```

## Terminal

I prefer [Ghostty](https://ghostty.org/) because: Ghostty is a fast, feature-rich, and cross-platform terminal emulator that uses platform-native UI and GPU acceleration.

Checkout their documentation for more info on what Ghostty can do: [https://ghostty.org/docsl]https://ghostty.org/docs)

```sh
brew install --cask ghostty
```

### Shell

Mac now comes with `zsh` as the default [shell](https://en.wikipedia.org/wiki/Comparison_of_command_shells). I use it with [Oh My Zsh](https://ohmyz.sh/).

#### Load dotfiles
All my dotfiles are stored on [github](https://github.com/barbar0jav1er/dotfiles).

I clone this repo to my machine and copy the files into my home directory.

### Github SSH Setup
* Follow [this guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to setup an ssh key for github
* Follow [this guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to add the ssh key to your github account

#### Other command line tools I use
 * [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)
 * [helm](https://helm.sh/)
 * [argocd](https://argo-cd.readthedocs.io/en/stable/cli_installation/)

 ```sh
 brew install helm
 brew install argocd
 brew install kubectl
 ```

 ## Node.js

I use fnm to manage the installed versions of Node.js on my machine. This allows me to easily switch between Node.js versions depending on the project I'm working in.

See installation instructions [here](https://github.com/Schniz/fnm).

```sh
brew install fnm
```
or

```sh
curl -fsSL https://fnm.vercel.app/install | bash
```
After the installation environment variables need to be setup before you can start using fnm. This is done by evaluating the output of fnm, add the following to your .zshrc profile:

`env. eval "$(fnm env --use-on-cd --shell zsh)"`

Now that nvm is installed, you can install a specific version of node.js and use it:

```sh
fnm install 20
nvm use 20
node --version
```

## VS Code
VS Code is my preferred code editor.

You can view all of my VS Code settings / extensions [here](https://github.com/barbar0jav1er/vscode-settings).