# Kartenspiel-Seite für die Spiele Schafkopf, Doppelkopf, Skat und (Bauern-)Schnapsen

# Inhalt
Die Seite <http://sauspiel.github.io/luschentreff.de/> ist eine Gemeinschaftsseite der Online-Spielplattformen Sauspiel, Skatstube, Fuchstreff und Bummerl und will die einzelnen Spiele vorstellen, Gemeinsamkeiten zeigen und das Erlernen der Spiele - insbesondere untereinander - erleichtern. 

# Umsetzung
Die Seite ist ersteinmal ein Blog, der sich Schafkopf, Skat, Doppelkopf und Schnapsen und allem was zum Kartenspielen dazugehört widmet. Dazu gibt es einen chronologischen Blog, der die Unterteilung in die Kategorien Schafkopf, Skat, Doppelkopf, Schnapsen und (alle) Kartenspiele (*) und eine Tag-Cloud hat. Später wären weitere Kategorien wie (Turnier-)Kalender, Registrierformular, o.ä denkbar.

# Technische Umsetzung

## Jekyll und Github-Pages
Die Seite wurde mit [Jekyll](http://jekyllrb.com/) erstellt und wird auf [Github-Pages](http://pages.github.com/) gehostet.

### Jekyll-Bootstrap
[Jekyll-Bootstrap](http://jekyllbootstrap.com) wurde eingesetzt um schnell eine gut vorformatierte Struktur zu erhalten, die leicht angepasst werden kann und sinnvolle rake-tasks besitzt.

## Benutzung

Da durch git push im master branch deployd wird sollte in einem anderen branch entwickelt werden. Neue Blog Posts werden im "posts"-branch vorgeschrieben und committed. Wenn ein Post online gestellt werden soll, kann dieser mittels cherry-pick in den master branch geholt werden.

### Jekyll Server starten
 
 	jekyll serve --watch
 	
	http://0.0.0.0:4000 (luschentreff.dev - siehe unten) im Browser aufrufen


### Neuen Post anlegen

	rake post title="Hello World"
	
### Neue Seite anlegen

	rake page name="Hello World"	
	
### Kategorien, Tags, Permalinks

Kategorien, Tags, Permalinks, etc werden im Header des Posts angelegt. Bsp.:

	---
	layout: post
	title: Schafkopf für Skatspieler
	description: Eine Einführung zum Schafkopfspielen für Skatspieler
	category: schafkopf
	tags: [schafkopf, skat, regeln]
	---

Meta-Title und Meta-Description können auch angegeben werden.

### Seite Deoployen

Der Branch "master" wird zum deployen verwendet. Nachdem Änderungen oder neue Inhalte erstellt wurden mit 

  jekyll serve

die statischen Seiten erstellen und mit

	git push

deployn.	


# Entwicklung

## Vorbereitung

### Repository "luschentreff.de" clonen

Das Projekt Luschentreff clonen

    mkdir ~/sauspiel
    cd ~/sauspiel
    git clone git@github.com:luschentreff/luschentreff.github.io.git
    
### Jekyll installieren

    gem install jekyll
        