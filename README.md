# images.paulrobertlloyd.com
⚠️ _DEPRECATED_ Image server for my personal website.

## Dependencies
  * [ImageMagick][1] (`brew install imagemagick`)
  * [ExifTool][2] (`brew install exiftool`)
  * [node.js and NPM][3]

## Installation
The image server uses [Converjon][4] for image conversion and caching. This process is managed on the server with [PM2][5]. Installing these dependancies with the `-g` flag ensures they can be run globally.

1. Ensure you have ImageMagick and ExifTool dependancies installed. **Converjon will silently fail without these packages present**.
2. Install Converjon and PM2 dependancies (`npm install`). Alternatively, installing these globally `npm install converjon -g &&  
npm install pm2 -g` will provide access on the command line.
3. Start the image server:
  * Production: `npm start`  
  * Development: `npm run start-dev`

_Note: the port used by converjon should be unique, i.e. not the same as that used in WebFaction application configuration._

[1]: http://www.imagemagick.org/script/binary-releases.php
[2]: http://www.sno.phy.queensu.ca/%7Ephil/exiftool/install.html
[3]: http://nodejs.org/download/
[4]: https://github.com/berlinonline/converjon
[5]: https://github.com/Unitech/pm2
