# tz - Get currently playing track on Tizonia
tz is a super simple shell script that outputs the currently playing track in Tizonia by analyzing Tizonia's output. I use it to show the currently playing track on my DWM status bar. It was written for using Tizonia with Spotify, but it is very easy to use it with other backends.

Here's is a screenshot taken from my own desktop.

![Screenshot](https://github.com/fstilman/tz/raw/master/screenshot.png)

## Configuration

All configuration is donde inside tz shell script. Almost no configuration is required. The most important one is setting TIZONIA_LOG to the path where Tizonia output is being sent. If you use tz for Spotify, you can also use the included commands "song", "artist", and "album" to launch Tizonia already redirecting its output to TIZONIA_LOG (this is simply done through tee).

```bash-script
# --- CONFIGURATION OPTIONS ----------------------------------------------------#
# File where tizonia will have its output redirected
TIZONIA_LOG=~/tizonia.out

# Available parameters for STATUS_FORMAT:
#   %TRACKNAME%
#   %ALBUM%
#   %ARTIST%
#   %TRACKNO%

STATUS_FORMAT="▶ %TRACKNAME% - %ARTIST%"
NO_TRACK="⏹ Not playing"
# -----------------------------------------------------------------------------#
```

## Usage

tz now: returns the currently playing track

tz song NAME

tz album NAME

tz artist NAME

tz list ID

Feel free to send any suggestions!
