# tracks and playlists

Build playlists for streaming services like <http://official.fm> and
<http://soundcloud.com>.

    $ pip install -r ./requirements.txt
    $ jot -w http://soundcloud.com/unsound/tracks?page=%.f 2 | xargs tracks | xargs playlist | tee mixes.xspf

[MPD](http://musicpd.org) supports (read only) XSPF, so you can drop the output
in your music directory, update your DB and `load` the `.xspf` file.
