# spotify-easyrpm

![img](https://i.imgur.com/y0tDlYD.png)

Spotify-easyrpm is a script which can download the latest debian package from the Spotify
repository and convert it into an RPM. It is also capable of installing, automated updating and storing
the Spotify RPMs in a local filesystem repo for installing Spotify updates alongside regular system updates


 Features

 * Set up a build enviornment on your PC and install rpm-build
 * Auto download the latest version of Spotify
 * Convert the debian package to RPM format
 * Install the Spotify RPM
 * Automated Spotify update check
 * Create a local filesystem repo so Spotify can be updated alongside regular updates
 * Fully unattended quiet mode


 Howto

  spotify-easyrpm

  - Regular prompt based mode to create an RPM and optionally install and create an update schedule

  spotify-easyrpm --quiet

  - Create the RPM
  - Install the Spotify RPM
  - Set up a update timer job
  - Set up a local filesystem repo

  spotify-easyrpm --create-schedule

  - If you previously opted out creating an automated update schedule but now desire it

  spotify-easyrpm --remove-schedule

  - Removes the schedule and local repo if present

  spotify-easyrpm --clean-repo

  - Cleans up the local filesystem repo


 Requirements

 * Latest openSUSE Leap / SLE (x86_64), or Tumbleweed (x86_64 or i586)


 Download links (One Click Install)

 * SLE 15 https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/openSUSE_Leap_15.0/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A15.0&query=spotify-easyrpm
 * openSUSE 15.0
 https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/openSUSE_Leap_15.0/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A15.0&query=spotify-easyrpm
 * openSUSE Tumbleweed https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/openSUSE_Tumbleweed/spotify-easyrpm.ymp?base=openSUSE%3AFactory&query=spotify-easyrpm


Auto Updates

spotify-easyrpm can create a systemd user timer job which will run 5 minutes after user login. 
This will call the script to do a light check against the Spotify debian repo for a new release.
If a new release is found, a build process is kicked off in the background and the final RPM will
be placed on your machine in a local filesystem repo (/var/cache/spotify-easyrpm).
The next time you run the system updater or zypper up you will see spotify-client appear as an
update alongside regular updates.

If you want to modify the update check timer, the file is at $HOME/.local/share/systemd/user/spotify-easyrpm.timer
Please see the systemd documentation for more information

If you want to see the output of the last update check or build process, you can run

journalctl --user-unit spotify-easyrpm