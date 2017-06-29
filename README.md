# spotify-easyrpm


Spotify-EasyRPM is a bash script designed to download the latest debian package from the Spotify repository and convert it into an RPM


 Features
 
 * Set up a build enviornment on your PC and install rpm-build 
 * Auto download the latest version of Spotify
 * Convert the debian package to RPM format
 * Install the Spotify RPM
 * Set up a weekly or monthly automated updated schedule via cron job (optional)
 * Create a local filesystem repo so Spotify can be updated alongside regular updates (optional)
 * Fully unattended mode (optional)


 Coming Soon (v0.7)!

 * Non Root mode - Do not require your sudo/su password. Spotify will install to your homedir. In this mode Spotify can still be automatically updated if desired!
 * Big code cleanup and reorg 


 Coming Soon (v0.8)!

 * Create a schedule switch - If you already have a generated spotify rpm installed but chose 'No' when prompted to create the schedule previously
 * Use a local copy of a Spotify deb - Useful if you want to stick to a specific Spotify version (perhaps pre v1.0.x)
 

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

