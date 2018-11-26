# spotify-easyrpm

![img](https://i.imgur.com/y0tDlYD.png)

Spotify-easyrpm is a script which can download the latest debian package from the Spotify
repository and convert it into an RPM. It is also capable of installing, scheduling and storing
the RPMs in a local filesystem repo for installing Spotify updates alongside regular system updates

Alternatively Spotify can be installed and run from your home folder which does not require you to give
root privileges to this script if you prefer


 Features

 * Set up a build enviornment on your PC and install rpm-build
 * Auto download the latest version of Spotify
 * Convert the debian package to RPM format
 * Install the Spotify RPM
 * Automated updated schedule via cron job (optional)
 * Create a local filesystem repo so Spotify can be updated alongside regular updates (optional)
 * Fully unattended mode (optional)
 * Install to home directory without root privileges


 Howto

  spotify-easyrpm

  - Regular prompt based mode to create an RPM and optionally install and create an update schedule

  spotify-easyrpm -noprompt

  - Create the RPM
  - Install the Spotify RPM
  - Set up a scheduled update job
  - Set up a local filesystem repo

  spotify-easyrpm -noroot

  - In this mode spotify-easyrpm will not require root/sudo
  - Spotify will run from your home folder
  - Schedule automatic updates (optional)
  - Not currently compatible with -noprompt mode

  spotify-easyrpm -noroot-uninstall

  - Removes Spotify from your homedir

  spotify-easyrpm -create-schedule

  - If you previously opted out creating an automated update schedule but now desire it

  spotify-easyrpm -remove-schedule

  - Removes the schedule and local repo if present

  spotify-easyrpm -clean-repo

  - Cleans up the local filesystem repo


 Requirements

 * Regular RPM mode - Latest openSUSE Leap (x86_64), Tumbleweed (x86_64 or i586) or SLE (x86_64)
 * NO ROOT mode - Any recent Linux distribution should work (only SUSE distros tested)


 Download links (One Click Install)

 * SLE 15 https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/openSUSE_Leap_15.0/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A15.0&query=spotify-easyrpm
 * openSUSE 15.0
 https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/openSUSE_Leap_15.0/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A15.0&query=spotify-easyrpm
 * openSUSE Tumbleweed https://software.opensuse.org/ymp/home:megamaced:spotify-easyrpm/openSUSE_Tumbleweed/spotify-easyrpm.ymp?base=openSUSE%3AFactory&query=spotify-easyrpm
