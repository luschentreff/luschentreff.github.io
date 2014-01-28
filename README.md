# Kartenspiel-Seite für die Spiele Schafkopf, Doppelkopf, Skat und (Bauern-)Schnapsen

# Inhalt
Die Seite <http://sauspiel.github.io/luschentreff.de/> ist eine Gemeinschaftsseite der Online-Spielplattformen Sauspiel, Skatstube, Fuchstreff und Bummerl und will die einzelnen Spiele vorstellen, Gemeinsamkeiten zeigen und das Erlernen der Spiele - insbesondere untereinander - erleichtern.

# Umsetzung
Die Seite ist ersteinmal ein Blog, der sich Schafkopf, Skat, Doppelkopf und Schnapsen und allem was zum Kartenspielen dazugehört widmet. Dazu gibt es einen chronologischen Blog, der die Unterteilung in die Kategorien Schafkopf, Skat, Doppelkopf, Schnapsen und (alle) Kartenspiele (*) und eine Tag-Cloud hat. Später wären weitere Kategorien wie (Turnier-)Kalender, Registrierformular, o.ä denkbar.

# Technische Umsetzung

## Jekyll und Github-Pages
Die Seite wurde mit [Jekyll](http://jekyllrb.com/) erstellt und wird auf [Github-Pages](http://pages.github.com/) gehostet.

### Jekyll-Bootstrap
[Jekyll-Bootstrap](http://jekyllbootstrap.com) wurde eingesetzt um schnell ein gut vorformatierte Struktur zu erhalten, die leicht angepasst werden kann und sinnvolle rake-tasks besitzt.

# Entwicklung

## Vorbereitung

### Repository "luschentreff.de" clonen

Den Ordner 'sauspiel' erstellen und das Repository luschentreff.de clonen

    mkdir ~/sauspiel
    cd ~/sauspiel
    git@github.com:sauspiel/luschentreff.de.git

### Jekyll installieren

    gem install jekyll

### NGINX konfigurieren
 * Datei etc/host öffnen:

    	sudo nano /private/etc/hosts

* folgende Zeile hinzufügen:

		127.0.0.1       luschentreff.dev

* nginx.conf öffnen:

		open /usr/local/etc/nginx/nginx.conf

* Folgendes hinzugügen, nicht vergessen <USERNAME> durch eigenen Username auszutauschen

	  server {

      	listen 80;
      	server_name luschentreff.dev;
      	root /Users/<USERNAME>/sauspiel/luschentreff.de;

      	location ~ .nginx.*.conf$ {
        	deny all;
      	}

      	include /Users/<USERNAME>/sauspiel/luschentreff.de/nginx_local.conf;

  	  }

## Benutzung

### Jekyll starten

 	jekyll serve --watch

	luschentreff.dev im Browser aufrufen

#### Fehlerbehebung
Sollte dieser Fehler auftreten:

	invalid byte sequence in US-ASCII

musst du folgende Befehle in der Console ausführen:

	export LANG=en_US.UTF-8
	export LANGUAGE=en_US.UTF-8
	export LC_ALL=en_US.UTF-8

### Neuen Post anlegen

	rake post title="Hello World"

### Neue Seite anlegen

	rake page name="Hello World"

### Kategorien und Tags
Kategorien und Tags werden im Header des Posts angelegt. Bsp.:

	---
	layout: post
	title: "Schafkopf für Skatspieler"
	description: "Eine Einführung zum Schafkopfspielen für Skatspieler"
	category: skat
	tags: [schafkopf, skat, regeln]
	---
Meta-Title und Meta-Description können auch angegeben werden.

### Seite Deoployen

Der Branch "gh-pages" wird zum deployen verwendet:

	git push origin gh-pages

