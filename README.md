# web-music-player

![logo](/display/files/favicon/favicon-16x16.png)
Web Music Player is a simple way to play your own music on any device connected to the web (pc, smartphone, tablet, ...).
It can work as a standalone application or in your smartphone browser.

You can manage your music with the [MusicBrainz](https://musicbrainz.org) API integration.

Live demo [here](http://nioc.github.io/web-music-player/).

## Installation and usage

Following example is based on Linux distribution with Apache :

1. Download the latest version [here](https://github.com/nioc/web-music-player/archive/master.tar.gz)
2. Untar the archive : `tar -xvzf web-music-player-master.tar.gz`
3. Move the files into you web server directory `mv web-music-player-master /var/www/wmp`
4. Fix file permissions `chown www-data:www-data /var/www/wmp -R`
5. Create database stuff using with the [database setup page](http://localhost/server/configuration/setup.php)
6. Update Admin user (edit password obviously)
7. Remove unnecessary files (/docs, /configuration/setup.php, ...)
8. Set your library folder
9. Enjoy :musical_note:

![menu](/docs/1-menu.png)
![player](/docs/2-player.png)
![playlist](/docs/3-playlist.png)
![library](/docs/4-library.png)
![album](/docs/5-library-album.png)
![folder](/docs/6-library-folder-add.png)
![profile](/docs/7-user-profile-edit.png)

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/nioc/web-music-player/tags).

## Authors

* **[Nioc](https://github.com/nioc/)** - *Initial work*

See also the list of [contributors](https://github.com/nioc/web-music-player/contributors) who participated in this project.

## Motivation

Our aim is to provide an easy to use web player able to handle a local catalog. Some awesome projects already exists but often with a complicated code.

## API

Please see [API description](API.md).


## Contributing

The project is open and any contribution is welcome!

To keep the code clean, we use [php-cs-fixer](http://cs.sensiolabs.org/), before commit launch this on each edited files:

```` bash
php /usr/local/bin/php-cs-fixer fix /path/to/editedFile.php -v --fixers=-psr0
````
You can handle all edited files with this single line:
```` bash
cd /var/www/wmp; for file in $(git diff-index --name-only HEAD); do php /usr/local/bin/php-cs-fixer fix "$file" -v --fixers=-psr0; done
````

A little how-to for github:

1. [Fork it](https://help.github.com/articles/fork-a-repo/)
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes (with a detailled message): `git commit -am 'Add an awesome feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

[![Build Status](https://travis-ci.org/nioc/web-music-player.svg?branch=master)](https://travis-ci.org/nioc/web-music-player)
[![Codacy Badge](https://api.codacy.com/project/badge/grade/615c9f1907364f9a8812298c11b8eb31)](https://www.codacy.com/app/nioc/web-music-player)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/fa150783-5bf2-4e9d-bcee-395401edf439/mini.png)](https://insight.sensiolabs.com/projects/fa150783-5bf2-4e9d-bcee-395401edf439)

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE.md) file for details

## Included project

This project includes the following:
- [Font Awesome](https://github.com/FortAwesome/Font-Awesome/)
- [AngularJS](https://github.com/angular/angular.js)
- [normalize.css](https://github.com/necolas/normalize.css)
- [getID3()](http://getid3.sourceforge.net)
- [Sortable](https://github.com/RubaXa/Sortable)
- [angular-loading-bar](https://github.com/chieffancypants/angular-loading-bar)
