# Run Spotify on a Raspberry Pi with Mopidy

## Set Up

### Install Raspian OS
[Install](https://www.raspberrypi.org/documentation/installation/installing-images/linux.md) a current **Raspian distribution**.

### Install Mopidy
[Install](https://docs.mopidy.com/en/latest/installation/debian/) **mopidy** for Raspian. The **Mopidy Jessie** version is supposed to work for **Raspian Stretch**.

## Install Soptify Plug In mopidy-spotify
[Install](https://github.com/mopidy/mopidy-spotify#installation) **mopidy-spotify**.

~~~
sudo apt-get install mopidy-spotify
~~~

**mopidy-spotify** needs some [config parameters](https://github.com/mopidy/mopidy-spotify#configuration).

### Install Web Front End mopidy-mopify
For [mopidy-music-webclient](https://docs.mopidy.com/en/latest/ext/web/#mopidy-musicbox-webclient) the `apt-get install` failed. Using `pip install` instead worked without problems.

~~~
pip install Mopidy-Mopify
~~~

## Trouble Shooting

### Group Configuration
When the Spotify plugin fails to play any track, add the service user to group **video**.

~~~
sudo usermod -G -a video mopidy
~~~
