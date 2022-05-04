# **SETTING-UP UBUNTU**

Ubuntu is built on Debian's architecture and infrastructure, and comprises Linux server, desktop and discontinued phone and tablet operating system versions.

## 1. Update the package lists

Downloads the package information from all configured sources. It is useful to get info on an updated version of packages or their dependencies.

```
sudo apt-get update
```

## 2. Install available upgrades of all packages

Install outdated packages, apply security patches for packages and keep your system secure, and find new packages to install.

New packages will be installed if required to satisfy dependencies, but existing packages will never be removed.

```
sudo apt-get upgrade
```

## 3. Custom the Ubuntu

### Animations

How to speed up Ubuntu by disabling animations. The animations when you open or minimize an application window, activities view, and "Show Applications" app menu can be disabled to speed up your system.

```
gsettings set org.gnome.desktop.interface enable-animations false
```

To restore changes

```
gsettings reset org.gnome.desktop.interface enable-animations
```

### Dock Transparency

Configure the dock launcher to make it transparent. Change your desired value ranging from 0 to 1, where 0 is totally transparent and 1 is opaque.

```
gsettings set org.gnome.shell.extensions.dash-to-dock background-opacity 1
```

To revert back to the default value (0.7)

```
gsettings reset org.gnome.shell.extensions.dash-to-dock background-opacity
```

### Dock Height Auto-resizing

The Dock is default extended to all the available screen heights. Make the Dock centered and its width is determined by the applications that you have open.

```
gsettings set org.gnome.shell.extensions.dash-to-dock extend-height false
```

And restore the change

```
gsettings set org.gnome.shell.extensions.dash-to-dock extend-height true
```

### Click to Minimize

When you click on an icon in the launcher, the application window appears in focus. If you click again on the icon of an application already in focus, the application window will be minimized.

```
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

If you do not like "click to minimize" behavior, you can set it back to default.

```
gsettings reset org.gnome.shell.extensions.dash-to-dock click-action
```

### Remove the "Show Application" icon

Remove the "Show Application" from the Dock.

```
gsettings set org.gnome.shell.extensions.dash-to-dock show-show-apps-button false
```

### Remove the "Home" icon

Remove the "Home" from the Desktop.

```
gsettings set org.gnome.shell.extensions.desktop-icons show-home false
```

### Remove the "Trash" icon

Remove the "Trash" from the Desktop.

```
gsettings set org.gnome.shell.extensions.desktop-icons show-trash false
```

## 4. Install Softwares

### Visual Studio Code

Visual Studio Code is a code editor redefined and optimized for building and debugging modern web and cloud applications. Visual Studio Code is free and available on your favorite platform - Linux, macOS, and Windows.

```
sudo snap install --classic code
```

### nvm

**nvm**, stand for Node Version Manager that allows you to quickly install and use different versions of Node via the command line.

Example:

```
$ nvm use 16
Now using node v16.9.1 (npm v7.21.1)
$ node -v
v16.9.1
$ nvm use 14
Now using node v14.18.0 (npm v6.14.15)
$ node -v
v14.18.0
$ nvm install 12
Now using node v12.22.6 (npm v6.14.5)
$ node -v
v12.22.6
```

To install or update nvm, you should run the `install-script.sh` file manually.

### npm

**npm** stands for Node Package Manager which is the default package manager for JavaScript's runtime NodeJS.

Download the latest version of npm

```
npm install -g npm
```

### NodeJS

NodeJS is a JavaScript runtime built on Chrome's V8 JavaScript engine.

```
sudo apt install nodejs
```

### Git

Git is a free and open-source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

```
sudo apt install git
```

Accompanying the configuration instructions in **Visual Studio Code**.

```
git config --global core.editor "code --wait"
```

### VLC Media Player

VLC is a free and open-source cross-platform multimedia player and framework that plays most multimedia files as well as DVDs, Audio CDs, VCDs, and various streaming protocols.

```
sudo snap install vlc
```

### OBS Studio

OBS (Open Broadcaster Software) is free and open source software for video recording and live streaming. Stream to Twitch, YouTube, and many other providers, or record your own videos with high-quality H264 / AAC encoding.

```
sudo snap install obs-studio
```

### IBus

IBus (Intelligent Input Bus) is an input method framework, a type of application that allows for easy switching between different keyboard layouts.

```
sudo apt-get install ibus-unikey

ibus-daemon -Rd

im-config
```
