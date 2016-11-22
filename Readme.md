# Random Hostname

In order to help anonymize more our connections: 

More helpful with conjuction with an already known project called [MacSpoof](https://github.com/feross/SpoofMAC "SoofMAC") that allows to randomize our mac address.

Randomizing our hostname will help a little more. My approach is to use a well now hostname *android-##########* that is popular nowadays.

This project is based on MacOSX, my current operating system, but can be populated to other OS's by applying some conditions and guessing the operating systems. 

It consist:

- Script that change current hostname in random way starting with "android-"
- a LaunchDaemon that runs on boot to help do this thing automatic on each boot

Any help is welcome as always

## Install

copy the script and the launchd configuration to their places, go to where this files are located in the Terminal *cd ~/Download/random-hostname* and then:

```
sudo cp random-hostname /usr/local/bin
sudo cp local.randomhostname.plist /Library/LaunchDaemons
sudo chmod 644 /Library/LaunchDaemons/local.randomhostname.plist
sudo chown root:wheel /Library/LaunchDaemons/local.randomhostname.plist
```

## Usage

Any time you want to change your Hostname you should run:

**random-hostname**