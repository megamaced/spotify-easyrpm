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
  - Set up a monthly scheduled update job
  - Set up a local filesystem repo

  spotify-easyrpm -noroot

  - In this mode spotify-easyrpm will not require root/sudo
  - Spotify will run from your home folder
  - Schedule automatic updates (optional)
  - Not currently compatible with -noprompt mode

  spotify-easyrpm -remove-schedule

  - Removes the schedule and local repo if present

 
 Coming Soon (v0.8)!

 * -create-schedule - If you already have a generated spotify rpm installed but chose 'No' when prompted to create the schedule previously
 * -uninstall - Remove Spotify from your homedir if installed with -noroot 
 * -localdeb - Use a local copy of a Spotify deb - Useful if you want to stick to a specific Spotify version (perhaps pre v1.0.x)
 

 Requirements

 * openSUSE 13.2 or later
 * SLE 12 or later


 Download links (One Click Install)

 * openSUSE 42.1 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.1/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.1&query=spotify-easyrpm
 * openSUSE 42.2 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.2/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.2&query=spotify-easyrpm
 * openSUSE 42.3 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.3/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.2&query=spotify-easyrpm
 * openSUSE Tumbleweed https://software.opensuse.org/ymp/home:megamaced/openSUSE_Tumbleweed/spotify-easyrpm.ymp?base=openSUSE%3AFactory&query=spotify-easyrpm


 Wishlist

 * Check the Spotify repository for available versions for comparision before attempting to download anything
 * Add support for other non Debian based distributions

