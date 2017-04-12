# spotify-easyrpm


Spotify-EasyRPM is a bash script designed to download the latest debian package from the Spotify repository and convert it into an RPM


 Features
 
 * Set up a build enviornment on your PC and install rpm-build 
 * Auto download the latest version of Spotify
 * Convert the debian package to RPM format
 * Install the Spotify RPM
 * Set up a weekly or monthly automated cron job
 * Create a local filesystem repo so Spotify can be updated alongside regular updates
 * Fully unattended mode

 Requirements

 * openSUSE 13.2 or later
 * SLE 12 or later


 Howto
 
 * Run `spotify-easyrpm` for the regular prompt mode
 * Run `spotify-easyrpm -noprompt` to accept the defaults (yes to install, yes to create the schedule)
 * Run `spotify-easyrpm -remove-schedule` to remove the cron job and local repo

 Download links (One Click Install)

 * openSUSE 42.1 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.1/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.1&query=spotify-easyrpm
 * openSUSE 42.2 https://software.opensuse.org/ymp/home:megamaced/openSUSE_Leap_42.2/spotify-easyrpm.ymp?base=openSUSE%3ALeap%3A42.2&query=spotify-easyrpm
 * openSUSE Tumbleweed https://software.opensuse.org/ymp/home:megamaced/openSUSE_Tumbleweed/spotify-easyrpm.ymp?base=openSUSE%3AFactory&query=spotify-easyrpm


 Wishlist

 * Check the Spotify repository for available versions for comparision before attempting to download anything
 * Add support for other non Debian based distributions
