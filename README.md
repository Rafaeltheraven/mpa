# Music Player Album
A series of bash scripts wrapped around `mpc` to facilitate listening to albums.

## Features

* Add a random album to the playlist
* Skip forward to the next album
* Whatever else I can think of that sounds useful

## How to use

`rand` - Adds a random album to the queue

`next` - Skips forward to the next album in the queue

Prepend any option with `-c` to clear the playlist up to the newly added/selected album. For example, `mpc -c next` will skip to the next album and clear all albums in the queue before it.

Options can also be chained, so `mpc rand next rand` will add a random album to the queue, skip to the next album, and then add a random album to the queue again.
