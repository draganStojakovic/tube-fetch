# tube-fetch

This shell script is inspired by [auto-ytdlp](https://github.com/exadisme/auto-ytdlp), so it borrows a lot from it. The main difference between the tube-fetch and auto-ytdlp is, tube-fetch uses a json file for storing information and the latter does not. I may add that auto-ytdlp is a lot more polished; tube-fetch will get there eventually.

## Dependencies:

- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [ffmpeg](https://github.com/FFmpeg/FFmpeg)
- [jq](https://github.com/stedolan/jq)

At first launch, script generates a JSON file and user is prompted to provied an absolute path to a directory where videos will be downloaded to.

How many days of videos, download directory and channels/playlists can be configured and it can be done either by manually editing generated json file (which is not recommended), or by running `tube-fetch` with flags. Run `tube-fetch -h` to find out more.

At first, channels list is empty, so user is required to add at least one valid YouTube link or playlist by running `tube-fetch -a`.  

tube-fetch downloads YouTube videos which it sources from channel links stored in a JSON file. The script and the data.json should not be separated.

### Important note:

This script assumes [yt-dlp](https://github.com/yt-dlp/yt-dlp) is in your PATH. In case it is not, either add it to your PATH, or modify *YTDLP* variable near the top of the file to include it.

## How to use:

```
Usage:
    tube-fetch                                      Checks for new videos and then downloads them.
    tube-fetch [options]"

Options:
    --help, -h                                      Help menu
    -l                                              Lists subscribed channels
    -a                                              Add achannel or playlist.
    -c                                              Configurehow many days back of videos should be downloaded.
    -d                                              Configurein which directory videos get downloaded to.
    -del                                            Deletes achannel or a playlist from a list.
```
