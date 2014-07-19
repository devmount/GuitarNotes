GuitarNotes
===========

A Plugin for moziloCMS 2.0

GuitarNotes provides various possibilities to display notes, tabs and pluck notation for guitar.

## Installation
#### With moziloCMS installer
To add (or update) a plugin in moziloCMS, go to the backend tab *Plugins* and click the item *Manage Plugins*. Here you can choose the plugin archive file (note that it has to be a ZIP file with exactly the same name the plugin has) and click *Install*. Now the GuitarNotes plugin is listed below and can be activated.

#### Manually
Installing a plugin manually requires FTP Access.
- Upload unpacked plugin folder into moziloCMS plugin directory: ```/<moziloroot>/plugins/```
- Set default permissions (chmod 777 for folders and 666 for files)
- Go to the backend tab *Plugins* and activate the now listed new GuitarNotes plugin

## Syntax
```{GuitarNotes|tab|<syntax>}```
With type ```tab```, a guitar tab can be inserted via a specific syntax. Notes with their position on the fretboard and their length can be specified.

1. Parameter ```<syntax>```: Notes are at least one number between 1 and 6 (corresponding guitar string) or number 0 (pause), directly followed by a letter that specifies the note value (w = whole note, h = half note, q = quarter note, e = eigth note, s = sixteenth note). Notes are seperated by white spaces, tacts are seperated by newlines. The following example syntax shows four tacts with different note variations:
```
{GuitarNotes|tab|
    654w
    42h 1h
    5q 1q 2q 3q
    0q 0e 2e 3e 1e 2e 3s 3s
}
```

```{GuitarNotes|pluck|<syntax>}```
With type ```pluck```, a guitar pluck diagram can be inserted via a specific syntax.

1. Parameter ```<syntax>```: Four different elements can be inserted (```.``` = Play Bass string, ```-``` = Pluck without touching the strings, ```V``` = Pluck back, ```A``` = Pluck forth), tacts are seperated by newlines, e.g.:
```
{GuitarNotes|pluck|
    .-.-A-AV
    AV.-AVAV
}
```

```{GuitarNotes|legend|<type>}```
Inserts a legend for each possible type.

1. Parameter ```<type>```: Possible types are ```tab``` and ```pluck```.

## License
This Plugin is distributed under *GNU General Public License, Version 3* (see LICENSE) or, at your choice, any further version.

## Documentation
A detailed documentation and demo can be found on DEVMOUNT's website:
http://devmount.de/Develop/moziloCMS/Plugins/GuitarNotes.html
