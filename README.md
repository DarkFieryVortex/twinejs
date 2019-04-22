## twinejs

Forked from [https://github.com/klembot/twinejs](https://github.com/klembot/twinejs)

### SYNOPSIS

This is a port of Twine to a browser and Electron app. See
[twinery.org](https://twinery.org) for more info.

The story formats in minified format under `story-formats/` exist in separate
repositories:

-   [Harlowe](https://bitbucket.org/_L_/harlowe)
-   [Paperthin](https://github.com/klembot/paperthin)
-   [Snowman](https://github.com/klembot/snowman)
-   [SugarCube](https://bitbucket.org/tmedwards/sugarcube)

### INSTALL

Run `npm install` at the top level of the directory.

### BUILDING

Run `npm start` to begin serving a development version of Twine to
http://localhost:8080. This server will automatically update with changes you
make.

To create a release, run `npm run build`. Finished files will be found under
`dist/`. In order to build Windows apps on OS X or Linux, you will need to have
[Wine](https://www.winehq.org/) and [makensis](http://nsis.sourceforge.net/)
installed. A file named `2.json` is created under `dist/` which contains
information relevant to the autoupdater process, and is currently posted to
https://twinery.org/latestversion/2.json.

To run the app in an Electron context, run `npm run electron`. `npm run electron-dev` is a bit faster as it skips minification.

`npm run lint` and `npm test` will lint and test the source code respectively.

`npm run pot` will create a POT template file for localization at
`src/locale/po/template.pot`. See Localization below for more information.

`npm run clean` will delete existing files in `build/` and `dist/`.
