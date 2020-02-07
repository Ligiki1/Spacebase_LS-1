# Dokumentation Stefan Reich und Ligia Dietze 

<img src="screenshot.png"/>

Hier sieht man unser selbstgecodetes Space invader spiel. Hier kann man mit einem Kleinen raumschif Die Angreifenden invader abschießen. Das Ganze wurde im Rahmen der Programmierpsrachen vorlesung an der HfG gMünd Programmiert. 
Die Inspiration sowie Gewissen Grundfunktionen (Raumschiff, Schießen und das Spielfenster) im Code wurden uns von Unserem Dozenten Florian Geiselhart gegeben.

## Usage / Benutzung

Um dieses Spiel zu Spielen muss man nur die github Repo Herunterladen und die index html in einem Browser öffnen. 
Gesteuert wird das ganze mit den Pfeiltasten un der Leertaste zum schießen. Bisher Verschwinden jedoch noch alle Spaceinvader auf einmal. Das liegt daran dass die Funktion zum einzelnen verschwinden lassen der jeweiligen invader noch nicht implementiert wurde.

## Structure / Aufbau

Hier werden kurz die Klassen und Funktionen beschrieben, die eine tragende Rolle in eurem großartigen Projekt spielen. 
Klassen können z.B. wie folgt kurz beschrieben werden:

* **Beer:** Eine Klasse um ein Bier in Code abzubilden. Enthält typische Eigenschaften von Bier:
  * `alcVol`: der Alkoholgehalt (Property)
  * `amount`: die Menge (Property, Standardwert: 500ml)

* **Person:** Eine Klasse um eine Person in Code abzubilden. Enthält typische Eigenschaften und Methoden von Menschen, um mit Bier zu interagieren:
  * `drinkBeer(beer)`: trinkt ein Bier, welches als Parameter übergeben wird und vom Typ / Klasse "Beer" sein muss (Funktion)
  * `isDrunk`: gibt an ob eine Person betrunken ist (Property, Boolean)

_Zentrale Funktionen (die nicht zu Klassen gehören) folgen dem selben Muster, werden aber meist etwas ausführlicher beschrieben:_

`haveParty(persons[], interval)`: Eine Funktion die ein Array von Personen entgegennimmt, und diese dann im angegebenen Intervall Bier trinken lässt. Nach jedem Durchlauf durch das Biertrinken (durch Aufruf von drinkBeer mit einem neu erzeugten Bier-Objekt) wird überprüft, ob die Anzahl der betrunkenen Personen größer 0 ist. Wenn dies eintritt, wird das Intervall bei jedem Durchlauf auf die doppelte Länge verlängert. Die Funktion endet in ihrer Ausführung dann wenn alle Personen isDrunk = true zurückgeben, oder wenn das Interval größer als 1 Stunde wird. Wird die Funktion mit nur einer Person im Array aufgerufen, wird eine Warnmeldung ausgegeben, um versehentliches Trinken alleine zu vermeiden. 

_(Achtung: Hier werden nur Funktionen beschrieben, die eine zentrale Rolle einnehmen.)_

Nach der Beschreibung der elementaren Bestandteile wird aus der Vogelperspektive nochmals beschrieben, welche Gesamtzustände euer System durchlaufen kann. In diesem Fall würde der User zunächst 0 bis n Personen erzeugen, und diese mit haveParty() zum Bier trinken bringen.  Dabei wird innerhalb von haveParty nacheinander für jede Person drinkBeer() aufgerufen, unter Benutzung von neuen Bier-Objekten. Nach Ende der Party muss das Programm neu gestartet werden um die Zustände zurückzusetzen.

_(Achtung, dieser Teil liest sich jetzt sehr ähnlich zur Funktionsbeschreibung von haveParty - das liegt daran dass es im Beispiel nur eine zentrale Funktion gibt. Ihr habt aber mehrere die zusammenspielen!)._

## ToDos

Was noch fehlt, und was die nächsten Schritte wären um es ggf. umzusetzen:
* Erweiterung der Party um Musik
* Berücksichtung individueller Verträglichkeiten von Bier in der Person-Klasse
* etc...
