# spotify-easyrpm

![img](https://i.imgur.com/y0tDlYD.png)

Spotify-easyrpm is a script which can download the latest debian package from the Spotify
repository and convert it into an RPM. It is also capable of installing, scheduling and storing
the RPMs in a local filesystem repo for installing Spotify updates alongside regular system updates


 Features

 * Set up a build enviornment on your PC and install rpm-build
 * Auto download the latest version of Spotify
 * Convert the debian package to RPM format
 * Install the Spotify RPM
 * Automated updated schedule via cron job (optional)
 * Create a local filesystem repo so Spotify can be updated alongside regular updates (optional)
 * Fully unattended mode (optional)


 Howto

  spotify-easyrpm

  - Regular prompt based mode to create an RPM and optionally install and create an update schedule

  spotify-easyrpm --quiet

  - Create the RPM
  - Install the Spotify RPM
  - Set up a scheduled update job
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
