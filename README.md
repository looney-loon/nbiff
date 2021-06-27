![nbiff logo](doc/logo.png) 

## Table of contents

- [nbiff](#nbiff)
- [Features](#features)
- [Online help](#online-help)
- [Software requirements](#software-requirements)
  - [Wayland support on GNOME](#wayland-support-on-gnome)
- [Installing / upgrading](#installing--upgrading)
- [Uninstalling](#uninstalling)
- [Customizing](#customizing)
- [Troubleshooting](#troubleshooting)
- [Development](#development)

## nbiff

`nbiff`, [good **new**
dawgy!](https://en.wikipedia.org/wiki/Biff_\(Unix\)), is
an intentionally simple, extensible systray email notifier. Geared for
Linux, yet it may (eventually) work on Windows.

## Features

`nbiff` has the following features:

- It self-adjusts when accounts and/or folders are created/deleted.
- It is designed to be light-weight and scalable.
- Largely it is immune from `Thunderbird`'s API changes.
- Supports both `x11` and `wayland`.
- The systray icon displays a status when there are **unread
  messages**.
- Further details are available by clicking on the icon and when
  supported, as a **tool tip**.
- User customizable systray icons.

## Online help

For online help, join the `nbiff`
[subreddit](https://www.reddit.com/r/nbiff).

## Software requirements

`Python 3` is required along with some additional libraries.  Choose
the desired method to install the necessary libraries:

| Method   | Information                                                  |
|----------|--------------------------------------------------------------|
| `pip`    | <pre lang="shell">pip3 install PyQt5 psutil</pre>            |
| Packages | <ul><li>python**X**-psutil</li><li>python**X**-qt5</li></ul> |
|          | where **X** matches the installed versions.                  |

### Wayland support on GNOME

Some **GNOME** versions require the `KStatusNotifierItem/AppIndicator
Support` extension for **Wayland** support.

Install it as follows:

1. [Go to the extension's webpage](https://extensions.gnome.org/extension/615/appindicator-support).
2. [Enable](https://github.com/pablo-blueoakdb/nbiff/blob/main/doc/KStatusNotifierItem.png)
   the extension by moving the slider to the **On** position.

## Installing / upgrading

The installation script handles installs and upgrades.

Below is how to install/upgrade:

1. [Get the latest the
   release](https://github.com/pablo-blueoakdb/nbiff/releases),
   uncompress the file and switch to the newly created directory.
2. Run the installer for your **email client** and follow the on-screen
   instructions:

   * `Thunderbird` <pre lang="shell">./Install_latest.tbird</pre>

## Uninstalling

1. Click on the systray icon and select the menu item `quit`.
2. Delete the code:
```shell
rm -rf ~/.nbiff
```

## Customizing

The following can be customized:

* The systray icons.
* Always ignore **unread messages** from a folder tree/name.

Details can be found [here](doc/CUSTOMIZING.md).

## Troubleshooting

Problems?  Head over to the [Troubleshooting](doc/TROUBLESHOOTING.md) document.

## Development

If you are interested in contributing, see the
[Development](src/README.md) document.
