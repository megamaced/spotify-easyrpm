# spotify-easyrpm


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
 * Set up a weekly or monthly automated updated schedule via cron job (optional)
 * Create a local filesystem repo so Spotify can be updated alongside regular updates (optional)
 * Fully unattended mode (optional)
 * Install to home directory without root privileges


 Howto

  spotify-easyrpm

  - Regular prompt based mode to create an RPM and optionally install and create an update schedule

  spotify-easyrpm -noprompt

  - Create the RPM
  - Install the Spotify RPM
  - Set up a weekly scheduled update job
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


 Coming Soon!

 * Fix NO ROOT desktop launcher if you don't have a $HOME/bin
 * The Packman spotify installer causes problems for spotify-easyrpm. We'll try to detect and clean up those problems
 * openSUSE 13.2 - Spotify now requires newer versions of mozilla-nspr and mozilla-nss. These are in home:megamaced. Spotify-easyrpm will automate those updates
 * Dependency warnings for noroot installs (If you installed spotify-easyrpm from OBS with recommends you will already have everything you need)
 * -localdeb - Use a local copy of a Spotify deb - Useful if you want to stick to a specific Spotify version (perhaps pre v1.0.x)


 Requirements

 * Regular RPM mode - openSUSE 13.2 or later, SLE 12 or later
 * NO ROOT mode - Any recent Linux distribution should work (only SUSE distros tested)


 Download links (One Click Install)

 * openSUSE 42.1 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.1/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.1&query=spotify-easyrpm
 * openSUSE 42.2 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.2/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.2&query=spotify-easyrpm
 * openSUSE 42.3 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.3/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.2&query=spotify-easyrpm
 * openSUSE Tumbleweed https://software.opensuse.org/ymp/home:megamaced/openSUSE_Tumbleweed/spotify-easyrpm.ymp?base=openSUSE%3AFactory&query=spotify-easyrpm
