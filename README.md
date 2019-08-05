# Music Player Album
A series of bash scripts wrapped around `mpc` to facilitate listening to albums.

## Features

* Add a random album to the playlist
* Skip forward to the next album
* Go to previous album
* See playlist as albums instead of tracks
* Whatever else I can think of that sounds useful

## How to use

`random [<query> <-t>]` - Adds a random album to the queue. You can pass along a search query to `mpc` using their search syntax. `-t` will add a single track instead of an album.  `-c` will clear the entire queue before adding.

`next` - Skips forward to the next album in the queue, `-c` will clear all albums before the newly selected one.

`prev` - Go to the previous album in the queue, `-c` does nothing.

`playlist` - Shows all the albums in the queue. This uses the `albumartist` tag, so please be sure that your music is properly tagged.

`current` - Show the currently playing album.

`queued` - Shows the album that is next in the queue.

`crop` - Remove all albums from the queue except for the current playing one

`play [index]` - Will play the `index`<sup>th</sup> album in the queue (1-index as `mpc` is). `-c` will remove all albums before this index. If no index is given, just plays index 1

`radio [<query> <-t>]` - Will simply run the `random` command consistently. Adding a new album/track when the previous one is finished.

Use the `-c` flag to remove albums from the queue. The exact effect depends on the command used, but overall, `-c` will remove all albums up to what has just been added/started.

Any `mpc` command can also be ran through `mpa`. Any argument prepended with `--` will also be passed along to `mpc` (for example, `--host` to designate a host).

## Requirements

Since this is basically just a wrapper around various `mpc` calls. If `mpc` works, `mpa` works. Meaning you will need

1. `mpd`

2. `mpc`

It should be noted, however, that `random` makes liberal use of the "new" `mcp` search expressions. If you want to make use of `random` and `radio`, you should have the following versions:

1. `mpd >= 0.21`

2. `libmpdclient >= 2.16`

3. `mpc >= 0.31`
