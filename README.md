# VVV Provision Flipper
:dolphin: Quickly toggle between different VVV provisioning scripts

[![Travis](https://img.shields.io/travis/bradp/vvv-provision-flipper.svg)]()


With VVV Provision Flipper, you can easily set up multiple named [Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV) provisioning scripts and toggle between them.

This is useful, as you can set a provisioning script, for example, that skips updating the included WordPress version to speed up the process. And then periodically toggle between the quick script and the default version included in VVV.

## Installation

If you have Homebrew installed, you run the following in your terminal application:

```
$ brew install bradp/vvv-provision-flipper/vvv-provision-flipper
```

Otherwise you'll want to clone and edit your $PATH to include the flip file.

## Usage

The first time you run 'flip' you will be prompted to confirm your VVV path. This process will also set up a 'scripts' folder inside of the provision folder in your VVV installation. Two files will be created, 'sample' and 'quick'. Sample will be a copy of the VVV provision script, ready for modifications. Quick is a trimmed-down version of default script.

By placing any scripts into this folder, you are able to quick use them as your main provison script by running `flip set <name>`.
To use the quicker version, simply run 'flip set quick'

To reset to using the normal provision script, simply run `flip reset`.
