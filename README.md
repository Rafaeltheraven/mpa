# Music Player Album
A series of bash scripts wrapped around `mpc` to facilitate listening to albums.

## Features

* Add a random album to the playlist
* Skip forward to the next album
* Go to previous album
* See playlist as albums instead of tracks
* Whatever else I can think of that sounds useful

## How to use

`random` - Adds a random album to the queue, `-c` will clear the entire queue before adding.

`next` - Skips forward to the next album in the queue, `-c` will clear all albums before the newly selected one.

`prev` - Go to the previous album in the queue, `-c` does nothing.

`playlist` - Shows all the albums in the queue.

`current` - Show the currently playing album.

`queued` - Shows the album that is next in the queue.

`status` - Simply shows `mpc status`

`crop` - Remove all albums from the queue except for the current playing one

`play [index]` - Will play the `index`<sup>th</sup> album in the queue (1-index as `mpc` is). `-c` will remove all albums before this index.

Use the `-c` flag to remove albums from the queue. The exact effect depends on the command used, but overall, `-c` will remove all albums up to what has just been added/started.

## Requirements

Since this is basically just a wrapper around various `mpc` calls. If `mpc` works, `mpa` works. Meaning you will need

1. `mpd`

2. `mpc`
