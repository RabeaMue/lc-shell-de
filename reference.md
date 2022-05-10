---
Layout: Referenz
Titel: Referenz
---

## Shell Cheat Sheet

_____
## Shell: Grundlagen

**`pwd`** - print working directory, aktuelles Verzeichnis ausgeben, indem ich mich gerade befinde

**`man`** - manual, zeigt das Benutzerhandbuch zu einem Befehel an

**`history`** - zeigt die History-Liste mit Zeilennummern an, verwende `n`, um die Liste zu begrenzen

**`ls`** - listet den Inhalt eines Verzeichnisses auf

- `ls -l` - listet Dateiinformationen auf
- `ls -lh` - listet menschenlesbare Dateiinformationen auf
- `ls -F` - listet Dateien und Verzeichnisse auf (Verzeichnisse haben ein abschließendes `/`)
- `ls -a` - alle Dateien auflisten, einschließlich versteckter Dateien
- `ls *.txt` - listet alle Dateien auf, die mit `.txt` enden

**`cd`** Verzeichnis wechseln

  `cd pathname` - führt dich in das durch `pathname` angegebene Verzeichnis
  
`cd ~` - führt dich in dein Home-Verzeichnis
  
  `cd ..` - führt dich ein Verzeichnis höher

______
### Shell: Interaktion mit Dateien

**`mkdir`** ein Verzeichnis erstellen

**`cat`** in die Shell ausgeben oder Datei(en) zur Ausgabe schicken 

**`head`** die ersten 10 Zeilen einer Datei oder mehrerer Dateien ausgeben

**`tail`** Ausgabe der letzten 10 Zeilen einer Datei oder mehrerer Dateien

**`mv`** Umbenennen oder Verschieben einer oder mehrerer Dateien. Syntax für das Umbenennen einer Datei: `mv FILENAME NEWFILENAME`

**`cp`** eine Sicherungskopie einer Datei oder mehrerer Dateien erstellen. Syntax: `cp FILENAME NEWFILENAME`

**`>`** Ausgabe umleiten. Syntax mit `cat`: `cat FILENAME1 FILENAME2 > NEWFILENAME`

**`>>`** Umleitung der Ausgabe durch Anhängen an den angegebenen Dateinamen. Syntax mit `cat`: `cat FILENAME1 FILENAME2 >> NEWFILENAME`

**`rm`** eine Datei oder mehrere Dateien entfernen. NB: *MIT ÄUSSERSTER VORSICHT VERWENDEN!!!*

**`rmdir -r`** löscht ein Verzeichnis, auch wenn es nicht leer ist.

**`rm -ri`** löscht ein Verzeichnis, auch wenn es nicht leer ist, fordert Sie aber auf, jeden Löschvorgang zu bestätigen.

**`touch`** aktualisiert die Zeitstempelinformationen von Dateien; erzeugt eine neue leere Datei touch FILENAME
______
### Shell: Wildcards

**`?`** ein Platzhalter für ein Zeichen oder eine Zahl

**`*`** ein Platzhalter für null oder mehr Zeichen oder Zahlen

**`[]`** definiert eine Klasse von Zeichen

*Beispiele*

- `foobar?`: findet 7-stellige Zeichenketten, die mit `foobar` beginnen und mit einem Zeichen oder einer Zahl enden
- `foobar*`: findet Zeichenfolgen, die mit `foobar` beginnen und mit null oder mehr anderen Zeichen oder Zahlen enden
- foobar*txt": passt zu Zeichenfolgen, die mit "foobar" beginnen und mit "txt" enden
- [1-9]foobar": findet Zeichenketten mit 8 Zeichen, die mit einer Zahl beginnen, nach der Zahl "foobar" enthalten und mit einem beliebigen Zeichen oder einer Zahl enden.

_____
### Shell: Zählen und Mining

**`wc`** Wörter zählen

- w": Wörter zählen
- l": Zeilen zählen
- `-c`: Zeichen zählen

**sort** Eingaben sortieren 

**`grep`** Globaler regulärer Ausdruck drucken

- `-c`: zeigt die Anzahl der Übereinstimmungen für jede Datei an
- `-i`: Übereinstimmung mit Unterscheidung von Groß- und Kleinschreibung
- `-w`: ganze Wörter abgleichen
- v": ausschließende Übereinstimmung
- `--file=FILENAME.txt`: verwendet die Datei `FILENAME.txt` als Quelle der in der Abfrage verwendeten Zeichenketten
- `|`: (vertikales Balkenzeichen) sendet die Ausgabe eines Befehls in einen anderen Befehl

_____
### Shell: Arbeiten mit freiem Text

**`sed`** wird verwendet, um Dateien zu modifizieren, verwenden Sie das `-e` Flag, um mehrere Befehle auszuführen

**`tr`** übersetzt oder löscht Zeichen in einer Datei

- `[:punct:]`: Interpunktionszeichen
- `[:upper:]`: Großbuchstaben
- `[:lower:]`: Kleinbuchstaben

**`'''\n`** übersetzt jedes Leerzeichen in `\n` und rendert es dann in eine neue Zeile

**`uniq`** meldet oder filtert wiederholte Zeilen in einer Datei, verwendet mit `-c`, um eine Wortzählung der Duplikate vorzunehmen
