# spotify-easyrpm

![img](https://i.imgur.com/y0tDlYD.png)

Spotify-easyrpm is a script which can download the latest debian package from the Spotify
repository and convert it into an RPM. It is also capable of installing, automated updating and storing
the Spotify RPMs in a local filesystem repo for installing Spotify updates alongside regular system updates


 ### Features

 * Set up a build enviornment on your PC and install rpm-build
 * Auto download the latest version of Spotify
 * Convert the debian package to RPM format
 * Install the Spotify RPM
 * Automated Spotify update check
 * Create a local filesystem repo so Spotify can be updated alongside regular updates
 * Fully unattended quiet mode


 ### News

  * 16/12/20 - We got accepted into the upcoming openSUSE Leap 15.3 oss repo!
  * 13/09/19 - We got accepted into openSUSE:Factory! We are now in the official Tumbleweed oss repo
  * 08/05/19 - We got accepted into multimedia:apps repo on the Open Build Service! I'm using their
    one click install links below where possible

 
 ### Howto

```bash
$> spotify-easyrpm
```
  - Regular prompt based mode to create an RPM and optionally install and create an update schedule

```bash
$> spotify-easyrpm --quiet
```

  - Create the RPM
  - Install the Spotify RPM
  - Set up a update timer job
  - Set up a local filesystem repo

```bash
$> spotify-easyrpm --create-schedule
```

  - If you previously opted out creating an automated update schedule but now desire it

```bash
$> spotify-easyrpm --remove-schedule
```

  - Removes the schedule and local repo if present

```bash
$> spotify-easyrpm --clean-repo
```

  - Cleans up the local filesystem repo


 ### Requirements

 * openSUSE Leap / SLE (x86_64), or Tumbleweed (x86_64 or i586)


 ### Auto Updates

    spotify-easyrpm can create a systemd user timer job which will run daily and 5 minutes after user login. 
    This will call the script to do a light check against the Spotify debian repo for a new release.
    If a new release is found, a build process is kicked off in the background and the final RPM will
    be placed on your machine in a local filesystem repo (/var/cache/spotify-easyrpm).
    The next time you run the system updater or zypper up you will see spotify-client appear as an
    update alongside regular updates.

    If you want to modify the update check timer, the file is at $HOME/.local/share/systemd/user/spotify-easyrpm.timer
    Please see the systemd documentation for more information

    To see a brief summary of the last run do

    systemctl --user status spotify-easyrpm

    If you want to see the full output of the last run you can do

    journalctl --user-unit spotify-easyrpm


 ### Download links (One Click Install)

 * [SLE 15](https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/SLE_15/spotify-easyrpm.ymp?base=SUSE%3ASLE-15%3AGA&query=spotify-easyrpm)
 * [openSUSE 15.1](https://software.opensuse.org/ymp/multimedia:apps/openSUSE_Leap_15.1/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A15.1&query=spotify-easyrpm)
 * [openSUSE 15.2](https://software.opensuse.org/ymp/multimedia:apps/openSUSE_Leap_15.2/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A15.2&query=spotify-easyrpm)
 * openSUSE Tumbleweed: We are included in Tumbleweed. Just a `zypper install spotify-easyrpm` to install
