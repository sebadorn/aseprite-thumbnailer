# Aseprite thumbnailer for GNOME

A thumbnailer for [Aseprite](https://aseprite.org) which generates thumbnails for `.aseprite` and `.ase` files (MIME type `application/octet-stream`).

Tested on Ubuntu 18.04.4 with GNOME 3.28.2.


## Requirements

* [Aseprite](https://aseprite.org) has to be installed and be executable with the command `aseprite`.
* GNOME as desktop environment.
* ImageMagick (`mogrify -scale`) to resize the thumbnail. Install with: `sudo apt install imagemagick`
	* Alternatively `ffmpeg` or `avconv` is used. One of both should already be installed per default.


## How to install

```bash
# 1. Copy the `aseprite-inofficial-thumbnailer` script to `/usr/bin/`.
sudo cp aseprite-inofficial-thumbnailer /usr/bin/
# 2. Make it executable.
sudo chmod +x /usr/bin/aseprite-inofficial-thumbnailer
# 3. Copy the `aseprite-inofficial.thumbnailer` to `/usr/share/thumbnailers/`.
sudo cp aseprite-inofficial.thumbnailer /usr/share/thumbnailers/
```

Then delete `~/.cache/thumbnails/fail/` so that all failed attempts to create a thumbnail are retried the next time the file is visible in the file viewer (probably Nautilus).


## How to uninstall

Delete the files:
* `/usr/share/thumbnailers/aseprite-inofficial.thumbnailer`
* `/usr/bin/aseprite-inofficial-thumbnailer`


## Resources

* https://aseprite.org/docs/cli/
* https://specifications.freedesktop.org/thumbnail-spec/thumbnail-spec-latest.html
* https://tecnocode.co.uk/2013/10/21/writing-a-gnome-thumbnailer/


## License

MIT License. See LICENSE file for details.
