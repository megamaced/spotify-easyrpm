# spotify-easyrpm

![img](https://i.imgur.com/y0tDlYD.png)

Spotify-EasyRPM is a script which automates the installing and updating of Spotify on openSUSE / SLE

## Features

* Auto download the latest version of Spotify from snapcraft.io
* Convert the snap package to RPM format
* Install the Spotify RPM
* Automated Spotify update check
* Update Spofity alongside your regular system updates
* Create a local filesystem repo
* Fully unattended quiet mode

## Howto

Regular prompt based mode to create an RPM and optionally install and create an update schedule:

```bash
$> spotify-easyrpm
```

Automate everything for me and don't ask questions:

```bash
$> spotify-easyrpm --quiet
```

Set either "edge" or "stable" version of Spotify client:

```bash
$> spotify-easyrpm --set-channel edge
```

Create a new update check schedule:

```bash
$> spotify-easyrpm --create-schedule
```

Remove the schedule and local repo if present:

```bash
$> spotify-easyrpm --remove-schedule
```

Clean up the local filesystem repo:

```bash
$> spotify-easyrpm --clean-repo
```

## Requirements

* openSUSE Leap / SLE, or Tumbleweed

## Auto Updates

spotify-easyrpm can create a systemd user timer job which will run daily and 5 minutes after user login.
This will call the script to do a light check against the Spotify debian repo for a new release.
If a new release is found, a build process is kicked off in the background and the final RPM will
be placed on your machine in a local filesystem repo (/var/cache/spotify-easyrpm).
The next time you run the system updater or zypper up you will see spotify-client appear as an
update alongside regular updates.

If you want to modify the update check timer, the file is at $HOME/.local/share/systemd/user/spotify-easyrpm.timer
Please see the systemd documentation for more information

To see a brief summary of the last run do

```bash
systemctl --user status spotify-easyrpm
```

If you want to see the full output of the last run you can do

```bash
journalctl --user-unit spotify-easyrpm
```

### How to install

* openSUSE : `zypper install spotify-easyrpm`
