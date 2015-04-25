# images.paulrobertlloyd.com

Image server for my personal website (in development).

## Dependencies

  * [ImageMagick][1]
  * [ExifTool][2] (at least version 9)
  * [node.js and NPM][3]

## Installation

The image server uses [Converjon][4] for image conversion and caching. This process is managed on the server with [PM2][5].

`npm install -g converjon`  
`npm install -g pm2`

## Usage

`pm2 start converjon.sh`

_Note: the port used by converjon should be unique, i.e. not the same as that used in WebFaction application configuration._

[1]: http://www.imagemagick.org/script/binary-releases.php
[2]: http://www.sno.phy.queensu.ca/%7Ephil/exiftool/install.html
[3]: http://nodejs.org/download/
[4]: https://github.com/berlinonline/converjon
[5]: https://github.com/Unitech/pm2
