---
title: "Arbeiten mit Dateien und Verzeichnissen"
teaching: 20
exercises: 10
questions:
- "Wie kann ich Dateien und Verzeichnisse kopieren, verschieben und löschen?"
- "Wie kann ich Dateien lesen?"
objectives:
- "Mit Dateien und Verzeichnissen über die Kommandozeile arbeiten"
- "Die Tabulatorvervollständigung verwenden, um die Eingabe einzuschränken"
- "Befehle verwenden, um Dateien und Teile von Dateien zu drucken und anzuzeigen"
- "Befehle verwenden, um Dateien zu verschieben/umzubenennen, zu kopieren und zu löschen".
keypoints:
- "Die Shell kann verwendet werden, um mehrere Dateien zu kopieren, zu verschieben und zu kombinieren"
---
## Mit Dateien und Ordnern arbeiten

Wir können nicht nur in Verzeichnissen navigieren, sondern auch mit Dateien auf der Kommandozeile arbeiten:
Wir können sie lesen, öffnen, ausführen und sogar bearbeiten. Genau genommen gibt es eigentlich
was wir in der Shell tun *können*, aber selbst erfahrene Shell-Benutzer wechseln immer noch zu
aber selbst erfahrene Shell-Benutzer wechseln für viele Aufgaben zu grafischen Benutzeroberflächen (GUIs), z. B. zum Bearbeiten von formatierten Text
Textdokumente (Word oder OpenOffice), das Surfen im Internet, die Bearbeitung von Bildern usw. Aber wenn wir
Aber wenn wir Hunderte von Bildern, z. B. die Seiten eines gescannten Buches, gleich zuschneiden wollen,
dann können wir diesen Beschnitt mit Hilfe von Shell-Befehlen automatisieren.

Bevor wir loslegen, verwenden wir `ls`, um zu überprüfen, wo wir uns befinden. Regelmäßig `ls` zu verwenden
zu verwenden, um deine Optionen einzusehen, ist nützlich, um sich zu orientieren. 

~~~
$ ls
~~~
{: .bash}
~~~
Anwendungen Dokumente Bibliothek Musik Öffentlich
Desktop Downloads Filme Bilder
~~~
{: .output}

Wir werden ein paar grundlegende Möglichkeiten ausprobieren, um mit Dateien zu interagieren. Wechseln wir zunächst in das
`shell-lesson` Verzeichnis auf deinem Desktop.

~~~
$ cd
$ cd Desktop/shell-lesson
$ pwd
~~~
{: .bash}
~~~
/Users/riley/Desktop/shell-lesson
~~~
{: .output}

Hier werden wir ein neues Verzeichnis erstellen und in dieses wechseln:

~~~
$ mkdir firstdir
$ cd firstdir
~~~
{: .bash}

Hier haben wir den Befehl `mkdir` (das bedeutet 'Verzeichnisse erstellen') verwendet, um ein Verzeichnis
namens "firstdir" erstellt. Dann haben wir den Befehl `cd` verwendet, um in dieses Verzeichnis zu wechseln.

Aber halt! Es gibt einen Trick, mit dem es etwas schneller geht. Lass uns ein Verzeichnis nach oben gehen.

~~~
$ cd ..
~~~
{: .bash}

Anstatt `cd firstdir` zu tippen, versuchen wir `cd f` einzugeben und drücken dann die Tabulatortaste.
Wir sehen, dass die Shell die Zeile zu `cd firstdir/` vervollständigt.

> ## Tabulator für automatische Vervollständigung
> Wenn du in der Shell die Tabulatortaste drückst, versucht sie, die Zeile anhand der
> die Zeile anhand der Dateien oder Unterverzeichnisse im aktuellen Verzeichnis automatisch zu vervollständigen.
> Wenn zwei oder mehr Dateien die gleichen Zeichen enthalten, wird die Autovervollständigung nur bis zum
> Danach können wir weitere Zeichen hinzufügen und es erneut mit Tabulator versuchen.
> erneut versuchen, Tabulator zu verwenden. Wir empfehlen, diese Methode heute zu verwenden.
> Wir empfehlen, diese Methode im Laufe des Tages anzuwenden, um zu sehen, wie sie sich verhält (denn sie spart eine Menge Zeit und Mühe!).
{: .callout}

### Dateien lesen

Wenn du dich in `firstdir` befindest, verwende `cd ..`, um zum Verzeichnis `shell-lesson` zurückzukehren.

Hier befinden sich Kopien von zwei gemeinfreien Büchern, die du vom
[Project Gutenberg] (https://www.gutenberg.org/) heruntergeladen wurden, sowie weitere Dateien, die wir
später behandeln werden.

~~~
$ ls -lh
~~~
{: .bash}
~~~
insgesamt 33M
-rw-rw-r-- 1 riley staff 383K Feb 22 2017 201403160_01_text.json
-rw-r--r-- 1 riley staff 3.6M Jan 31 2017 2014-01-31_JA-africa.tsv
-rw-r--r-- 1 riley staff 7.4M Jan 31 2017 2014-01-31_JA-america.tsv
-rw-rw-r-- 1 riley staff 125M Jun 10 2015 2014-01_JA.tsv
-rw-r--r-- 1 riley staff 1.4M Jan 31 2017 2014-02-02_JA-britain.tsv
-rw-r--r-- 1 riley staff 582K Feb 2 2017 33504-0.txt
-rw-r--r-- 1 riley staff 598K Jan 31 2017 829-0.txt
-rw-rw-r-- 1 riley staff 18K Feb 22 2017 tagebuch.html
drwxr-xr-x 1 riley staff 64B Feb 22 2017 firstdir
~~~
{: .output}

Die Dateien `829-0.txt` und `33504-0.txt` enthalten den Inhalt von Buch #829
und #33504 auf Project Gutenberg. Aber wir haben vergessen, *welche* Bücher, also
versuchen wir den Befehl `cat`, um den Text der ersten Datei zu lesen:

~~~
$ cat 829-0.txt
~~~
{: .bash}

Das Terminalfenster bricht auf und das ganze Buch wird übersprungen (es wird in deinem Terminal ausgedruckt).
dein Terminal) und hinterlässt uns eine neue Eingabeaufforderung und die letzten Zeilen des Buches
über dieser Eingabeaufforderung.

Oft wollen wir nur einen kurzen Blick auf den ersten oder letzten Teil einer Datei werfen, um
einen Eindruck davon zu bekommen, worum es in der Datei geht. Damit wir das tun können, stellt uns die Unix-Shell
die Befehle `head` und `tail` zur Verfügung.

~~~
$ head 829-0.txt
~~~
{: .bash}
~~~
Das Project Gutenberg eBook, Gullivers Reisen, von Jonathan Swift


Dieses eBook kann von jedermann überall kostenlos und ohne
und fast ohne jegliche Einschränkungen.  Du kannst es kopieren, weitergeben oder
unter den Bedingungen der Project Gutenberg Lizenz verwenden, die diesem eBook
die diesem eBook beiliegt oder online unter www.gutenberg.org
~~~
{: .output}

Dies gibt einen Blick auf die ersten zehn Zeilen,
während `tail 829-0.txt` eine Perspektive auf die letzten zehn Zeilen bietet:

~~~
$ tail 829-0.txt
~~~
{: .bash}
~~~
Die meisten Leute fangen auf unserer Website an, auf der die wichtigste PG-Suchfunktion zu finden ist:

    http://www.gutenberg.org

Diese Website enthält Informationen über das Projekt Gutenberg-tm,
wie man an die Project Gutenberg Literary Archive Foundation spenden kann
Stiftung Projekt Gutenberg-Archiv spenden kann, wie du bei der Produktion unserer neuen eBooks helfen kannst und wie du
wie du dich für unseren E-Mail-Newsletter anmelden kannst, um über neue eBooks informiert zu werden.
~~~
{: .output}

Wenn zehn Zeilen nicht ausreichen (oder zu viel sind), sollten wir `man head` (oder `head --help`, wenn du Windows verwendest) prüfen
um zu sehen, ob es eine Option gibt, mit der man die Anzahl der Zeilen angeben kann
(die gibt es: `head -n 20` gibt 20 Zeilen aus).

Eine andere Möglichkeit, durch die Dateien zu navigieren, ist, sich den Inhalt Bildschirm für Bildschirm anzusehen.
Tippe `less 829-0.txt`, um den ersten Bildschirm zu sehen, `Leertaste`, um den
um den nächsten Bildschirm zu sehen und so weiter, dann `q` zum Beenden (zurück zur Eingabeaufforderung).

~~~
$ less 829-0.txt
~~~
{: .bash}

Wie viele andere Shell-Befehle können auch die Befehle `cat`, `head`, `tail` und `less`
eine beliebige Anzahl von Argumenten entgegennehmen (sie können mit beliebig vielen Dateien arbeiten).
Wir werden sehen, wie wir die ersten Zeilen von mehreren Dateien auf einmal abrufen können.
Um uns das Tippen zu ersparen, führen wir zunächst einen sehr nützlichen Trick ein.

> ## Wiederverwendung von Befehlen
> In einer leeren Eingabeaufforderung drückst du die Pfeiltaste nach oben und bemerkst, dass der vorherige
> Befehl, den du eingegeben hast, vor deinem Cursor erscheint. Wir können weiter die
> Pfeil nach oben drücken, um durch deine vorherigen Befehle zu gehen. Der Pfeil nach unten führt zurück
> zu deinem letzten Befehl. Das ist eine weitere wichtige arbeitssparende
> Funktion, die wir oft verwenden werden.
{: .callout}

Drücke den Pfeil nach oben, bis du zum Befehl "head 829-0.txt" kommst. Füge ein Leerzeichen
und dann `33504-0.txt` (Erinnerst du dich an deinen Freund Tab? Tippe `3` gefolgt von Tab, um
um `33504-0.txt` zu erhalten), um den folgenden Befehl zu erhalten:

~~~
$ head 829-0.txt 33504-0.txt
~~~
{: .bash}
~~~
==> 829-0.txt <==
Das Project Gutenberg eBook, Gullivers Reisen, von Jonathan Swift


Dieses eBook kann von jedermann überall kostenlos und mit
fast ohne Einschränkungen.  Du kannst es kopieren, weitergeben oder
unter den Bedingungen der Project Gutenberg Lizenz verwenden, die diesem eBook
die diesem eBook beiliegt oder online unter www.gutenberg.org




==> 33504-0.txt <==
Das Project Gutenberg EBook von Opticks, von Isaac Newton

Dieses eBook kann von jedermann überall kostenlos und mit
fast ohne Einschränkungen.  Du darfst es kopieren, weitergeben oder
unter den Bedingungen der Project Gutenberg-Lizenz weiterverwenden, die diesem eBook
die diesem eBook beiliegt oder online unter www.gutenberg.org


Titel: Opticks
       oder, eine Abhandlung über die Spiegelungen, Brechungen und Beugungen,
~~~
{: .output}

Soweit alles gut, aber wenn wir *viele* Bücher hätten, wäre es mühsam, alle Dateinamen einzugeben.
alle Dateinamen einzugeben. Zum Glück unterstützt die Shell Wildcards! Das `?` (entspricht genau
ein Zeichen) und `*` (passt auf null oder mehr Zeichen) kennst du wahrscheinlich
von Suchsystemen für Bibliotheken. Wir können den Platzhalter `*` verwenden, um den obigen `head`
Befehl kompakter zu formulieren:

~~~
$ head *.txt
~~~
{: .bash}

> ## Mehr über Wildcards
> Wildcards sind eine Funktion der Shell und funktionieren daher mit *jedem* Befehl.
> Die Shell expandiert Wildcards zu einer Liste von Dateien und/oder Verzeichnissen, bevor
> bevor der Befehl ausgeführt wird, und der Befehl sieht die Wildcards nie.
> Wenn ein Platzhalterausdruck auf keine Datei passt, gibt die Bash den Ausdruck als Parameter weiter.
> den Ausdruck als Parameter an den Befehl weiter, wie er ist. Zum Beispiel
> Die Eingabe von `ls *.pdf` führt zu einer Fehlermeldung, dass es keine Datei namens *.pdf gibt.
{: .callout}


<!-- Timing: Ich habe 75 Minuten gebraucht, um hierher zu kommen -->

### Verschieben, Kopieren und Löschen von Dateien

Vielleicht wollen wir auch den Dateinamen in etwas Beschreibenderes ändern.
Wir können sie unter einem neuen Namen **verschieben**, indem wir den Befehl `mv` oder move verwenden,
Wir geben den alten Namen als erstes Argument und den neuen Namen als zweites Argument an
Argument:

~~~
$ mv 829-0.txt gulliver.txt
~~~
{: .bash}

Dies entspricht der Funktion "Datei umbenennen".

Wenn wir danach einen `ls`-Befehl ausführen, werden wir sehen, dass die Datei jetzt `gulliver.txt` heißt:

~~~
$ ls
~~~
{: .bash}
~~~
2014-01-31_JA-africa.tsv 2014-02-02_JA-britain.tsv gulliver.txt
2014-01-31_JA-america.tsv 33504-0.txt
2014-01_JA.tsv
~~~
{: .output}

> ## Kopieren einer Datei
>
> Anstatt eine Datei zu *verschieben*, möchtest du vielleicht eine Datei *kopieren* (ein Duplikat erstellen),
> zum Beispiel, um ein Backup zu erstellen, bevor du eine Datei änderst.
> Genau wie der Befehl `mv` benötigt der Befehl `cp` zwei Argumente: den alten Namen
> und den neuen Namen. Wie würdest du eine Kopie der Datei `gulliver.txt` mit dem Namen
> `gulliver-backup.txt`? Versuche es!
>
> > ## Antwort
> > ~~~
> > cp gulliver.txt gulliver-backup.txt
> > ~~~
> > {: .bash}
> {: .solution}
{: .challenge}

> ## Umbenennen eines Verzeichnisses
>
> Das Umbenennen eines Verzeichnisses funktioniert genauso wie das Umbenennen einer Datei. Versuche, den Befehl
> `mv` Befehl, um das Verzeichnis `firstdir` in `backup` umzubenennen.
>
> > ## Antwort
> > ~~~
> > mv firstdir backup
> > ~~~
> > {: .bash}
> {: .solution}
{: .challenge}

> ## Verschieben einer Datei in ein Verzeichnis
>
> Wenn das letzte Argument, das du dem `mv`-Befehl gibst, ein Verzeichnis und keine Datei ist,
> wird die Datei, die im ersten Argument angegeben ist, in dieses Verzeichnis verschoben. Versuche
> den Befehl `mv` zu verwenden, um die Datei `gulliver-backup.txt` in den
> `backup` Ordner zu verschieben.
>
> > ## Antwort
> > ~~~
> > mv gulliver-backup.txt backup
> > ~~~
> > {: .bash}
> >
> > Das würde auch funktionieren:
> >
> > ~~~
> > mv gulliver-backup.txt backup/gulliver-backup.txt
> > ~~~
> > {: .bash}
> {: .solution}
{: .challenge}

> ## Die Wildcards und regulären Ausdrücke
>
> Der Platzhalter `?` passt auf ein Zeichen. Der Platzhalter "*" passt auf null oder
> mehr Zeichen. Wenn du an der Lektion über reguläre Ausdrücke teilgenommen hast, weißt du
> erinnerst du dich, wie du das als reguläre Ausdrücke ausdrücken würdest?
>
> (Reguläre Ausdrücke sind keine Funktion der Shell, aber einige Befehle unterstützen
> sie. Darauf kommen wir noch zurück.)
>
> > ## Antwort
> > * Der Platzhalter `?` passt auf den regulären Ausdruck `.` (ein Punkt)
> > * Der Platzhalter `*` entspricht dem regulären Ausdruck `.*`
> {: .solution}
{: .challenge}

> ## Verwendung von `history`
> Verwende den Befehl `history`, um eine Liste aller Befehle zu sehen, die du während der 
> aktuellen Sitzung eingegeben hast. Du kannst auch <kbd>Strg</kbd> + <kbd>r</kbd> verwenden, um einen Rückwärtssuchlauf durchzuführen. Drücke <kbd>Strg</kbd> + <kbd>r</kbd>, 
> und beginne dann, einen beliebigen Teil des Befehls einzugeben, den du suchst. Der vergangene Befehl wird 
> automatisch vervollständigt. Drücke "Enter", um den Befehl erneut auszuführen, oder drücke die Pfeiltasten, um den Befehl zu > bearbeiten. 
> Bearbeiten des Befehls. Wenn mehrere vergangene Befehle den von dir eingegebenen Text enthalten, kannst du 
> <kbd>Strg</kbd> + <kbd>r</kbd> wiederholt drücken, um sie durchzugehen. Wenn du nicht finden kannst, wonach du suchst 
> in der Rückwärtssuche nicht findest, verwende <kbd>Strg</kbd> + <kbd>c</kbd>, um zur Eingabeaufforderung zurückzukehren. Wenn du den Verlauf speichern willst 
> deinen Verlauf speichern willst, um vielleicht einige Befehle zu extrahieren, aus denen du später ein Skript bauen kannst, kannst du 
> kannst du das mit `history > history.txt` tun. Dies gibt den gesamten Verlauf in eine Textdatei 
> namens `history.txt`, die du später bearbeiten kannst. Um einen Befehl aus der History aufzurufen, gibst du 
> `History` ein. Notiere die Befehlsnummer, z.B. 2045. Rufe den Befehl auf, indem du 
> `!2045`. Dadurch wird der Befehl ausgeführt.
{: .challenge}

> ## Den Befehl `echo` verwenden
> Der Befehl "echo" gibt einfach einen Text aus, den du angibst. Probiere es aus: `echo 'Library Carpentry is awesome!'`.
> Interessant, nicht wahr?
>
> Du kannst auch eine Variable angeben. Tippe zuerst `NAME=`, gefolgt von deinem Namen, und drücke die Eingabetaste.
> Gib dann `echo "$NAME ist ein fantastischer Bibliotheksschüler"` ein und drücke die Eingabetaste. Was passiert?
>
> Du kannst sowohl Text- als auch normale Shell-Befehle mit `echo` verwenden, zum Beispiel den
> `pwd`-Befehl, den du heute schon gelernt hast. Das machst du, indem du einen Shell
> Befehl in `$(` und `)` einschließt, zum Beispiel `$(pwd)`. Probiere nun Folgendes aus:
> `echo "Endlich ist es schön und sonnig am" $(Datum)`.
> Beachte, dass die Ausgabe des Befehls `date` zusammen mit dem Text
> den du angegeben hast. Das Gleiche kannst du mit einigen anderen Befehlen ausprobieren, die du bisher gelernt hast.
>
> **Warum denkst du, dass der echo-Befehl in der Shell-Umgebung eigentlich so wichtig ist?**
>
> > ## Antwort
> > Du denkst vielleicht, dass ein so einfacher Befehl wie `echo` nicht viel wert ist. Aber von dem Moment an, in dem du
> > anfängst, automatisierte Shell-Skripte zu schreiben, wird er sehr nützlich. Zum Beispiel benötigst du oft den Befehl
> > Text auf dem Bildschirm ausgeben, zum Beispiel den aktuellen Status eines Skripts.
> >
> > Außerdem hast du gerade zum ersten Mal eine Shell-Variable verwendet, die du zum vorübergehenden Speichern von Informationen verwenden kannst,
> > die du später wiederverwenden kannst. Das gibt dir viele Möglichkeiten, sobald du anfängst, automatisierte Skripte zu schreiben.
> {: .solution}
{: .challenge}

Zum Schluss noch etwas zum Löschen. Wir werden es jetzt nicht verwenden, aber wenn du eine Datei löschen willst,
aus welchem Grund auch immer, lautet der Befehl `rm`, oder remove.

Wenn wir Platzhalter verwenden, können wir sogar viele Dateien löschen. Und mit dem Flag "r" können wir
können wir Ordner mit ihrem gesamten Inhalt löschen.

**Anders als beim Löschen aus unserer grafischen Benutzeroberfläche gibt es *keine* Warnung,
*keinen* Papierkorb, aus dem du die Dateien zurückholen kannst und keine anderen Rückgängigmach-Optionen!**
Sei deshalb bitte sehr vorsichtig mit `rm` und extrem vorsichtig mit `rm -r`.
