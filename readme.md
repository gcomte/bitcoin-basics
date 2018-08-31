# ndbjs Sprint Review

Reveal.js Slides für die Sprint Reviews Ndbjs

## Installation

Es wird nodejs und grunt-cli benötigt. Die Installation von Nodejs erfolgt am einfachsten über den Node Version Manager:

https://github.com/creationix/nvm


```
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash
$ nvm install stable
$ nvm use stable
$ npm install -g grunt-cli
```


Danach kann die Präsentation lokal gestartet werden:

```
$ cd path/to/your/local/repo
$ npm install
$ grunt serve
```

Der Grunt Task (serve) buildet und lädt die Präsentation neu im Browser, wenn eine Datei angepasst wird.

## Problem solving

Bei Problemen beim Start der Folien (wiederholtes starten mit ```ENOSPC``` error) hilft das Setzen des Wertes ```max_user_watches``` gemäss [Stakeoverflow](https://stackoverflow.com/questions/22475849/node-js-error-enospc).


## How-To

### Markdown
Die Folien werden in Markdown in der Datei sprint-review.md erstellt.

[Markdown Cheatsheet](https://duckduckgo.com/?q=markdown+cheatsheet&t=canonical&ia=answer&iax=1)

### Sections, Slides und Styles

Einzelne Folien (Slides) sind in Abschnitten (Sections) organisiert.
Neue Sections und Slides werden im mit html-kommentaren unterteilt und mit einem Style versehen, wobei die Style-Class **nach** dem Inhalt der Folie angegeben werden muss.

```
<!-- section -->
### Section Header
<!-- .slide: class="master03" -->

<!-- slide -->
### Slide 1
<!-- .slide: class="master01" -->

<!-- slide -->
### Slide 2
<!-- .slide: class="master02" -->

```


### Screenshots

Screenshots werden im Verzeichnis `assets` abgelegt und können wie folgt eingebunden werden:

```
![](/assets/screenshot.png)
```

### ...
