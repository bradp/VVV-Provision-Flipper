# VVV Provision Flipper
:dolphin: Quickly toggle between different VVV provisioning scripts

[![Travis](https://img.shields.io/travis/bradp/vvv-provision-flipper.svg)]()


With VVV Provision Flipper, you can easily set up multiple named [Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV) provisioning scripts and toggle between them.

This is useful, as you can set a provisioning script, for example, that skips updating the included WordPress version to speed up the process. And then periodically toggle between the quick script and the default version included in VVV.

## Installation

To install, you'll want to add the `flip` file above to your `$PATH`. In your terminal, simply do `$ echo $PATH` and save [flip](https://raw.githubusercontent.com/bradp/vvv-provision-flipper/master/flip) in one of those folders. You may have to `$ chmod +x flip` in the directory you save as well.

Homebrew installation is planned for the near future.

## Usage

The first time you run 'flip' you will be prompted to confirm your VVV path. This process will also set up a 'scripts' folder inside of the provision folder in your VVV installation. Two files will be created, 'sample' and 'quick'. Sample will be a copy of the VVV provision script, ready for modifications. Quick is a trimmed-down version of default script.

By placing any scripts into this folder, you are able to quick use them as your main provison script by running `flip set <name>`.
To use the quicker version, simply run 'flip set quick'

To reset to using the normal provision script, simply run `flip reset`.
