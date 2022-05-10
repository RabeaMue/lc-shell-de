---
title: "Navigieren im Dateisystem"
teaching: 20
exercises: 10
questions:
- "Wie bewegst du dich im Dateisystem in der Shell?"
objectives:
- "Shell-Befehle verwenden, um mit Verzeichnissen und Dateien zu arbeiten"
- "Shell-Befehle verwenden, um Daten zu finden und zu manipulieren"
keypoints:
- "Zu wissen, wo du dich in deiner Verzeichnisstruktur befindest, ist der Schlüssel zur Arbeit mit der Shell"
---

## Navigieren in der Shell

Wir beginnen mit den Grundlagen der Navigation in der Unix-Shell.

Beginnen wir damit, die Shell zu öffnen. Dann siehst du wahrscheinlich ein schwarzes Fenster mit einem blinkenden Cursor neben einem Dollarzeichen.
Das ist unsere Befehlszeile und das "$" ist der Befehl **prompt**, um zu zeigen, dass das System bereit für unsere Eingabe ist.
Das Aussehen der Eingabeaufforderung variiert von System zu System, je nachdem, wie das System konfiguriert wurde,
aber normalerweise endet er mit einem "$".

Wenn du in der Shell arbeitest, befindest du dich immer *irgendwo* im Dateisystem deines Computers
Dateisystem, in einem Ordner (Verzeichnis). Deshalb werden wir zunächst herausfinden
Du kannst den Befehl `pwd` verwenden, wenn du dir nicht sicher bist, wo du dich befindest.
wo du dich befindest. Er steht für "print working directory" und das Ergebnis des
Befehls wird auf deiner Standardausgabe, also dem Bildschirm, ausgegeben.

Gib `pwd` ein und drücke Enter, um den Befehl auszuführen
(Beachte, dass das `$`-Zeichen verwendet wird, um einen Befehl anzuzeigen, der in der Eingabeaufforderung eingegeben werden muss,
 Wir geben aber nie das "$"-Zeichen selbst ein, sondern nur das, was danach kommt.):

~~~
$ pwd
~~~
{: .bash}
~~~
/Users/riley
~~~
{: .output}

Die Ausgabe wird ein Pfad zu deinem Heimatverzeichnis sein. Lass uns überprüfen, ob wir es erkennen
indem wir uns den Inhalt des Verzeichnisses ansehen. Dazu verwenden wir den Befehl `ls`. Das steht für "list" und das Ergebnis ist ein Ausdruck aller Inhalte in dem Verzeichnis:

~~~
$ ls
~~~
{: .bash}
~~~
Anwendungen Dokumente Bibliothek Musik Öffentlich
Desktop Downloads Filme Bilder
~~~
{: .output}

Vielleicht wollen wir mehr Informationen als nur eine Liste von Dateien und Verzeichnissen.
Das können wir erreichen, indem wir verschiedene **Flags** (auch bekannt als `Optionen`, `Parameter`, oder, am häufigsten
Argumente") zu unseren Grundbefehlen hinzufügen.
Argumente verändern die Funktionsweise des Befehls, indem sie dem Computer mitteilen, welche Art von Ausgabe oder Manipulation wir wünschen.

Wenn wir `ls -l` eingeben und die Eingabetaste drücken, gibt der Computer eine Liste von Dateien aus, die
Informationen, die denen im Finder (Mac) oder Explorer (Windows) ähneln:
die Größe der Dateien in Bytes, das Datum der Erstellung oder der letzten Änderung und den Dateinamen.

~~~
$ ls -l
~~~
{: .bash}
~~~
gesamt 0
drwx------+ 6 riley staff 204 Jul 16 11:50 Desktop
drwx------+ 3 riley staff 102 Jul 16 11:30 Dokumente
drwx------+ 3 riley staff 102 Jul 16 11:30 Downloads
drwx------@ 46 riley staff 1564 Jul 16 11:38 Bibliothek
drwx------+ 3 riley staff 102 Jul 16 11:30 Filme
drwx------+ 3 riley staff 102 Jul 16 11:30 Musik
drwx------+ 3 riley staff 102 Jul 16 11:30 Bilder
drwxr-xr-x+ 5 riley staff 170 Jul 16 11:30 Public
~~~
{: .output}

Im alltäglichen Gebrauch sind wir eher an Maßeinheiten wie Kilobyte, Megabyte und Gigabyte gewöhnt.
Zum Glück gibt es ein weiteres Flag `-h`, das, wenn es zusammen mit der Option -l verwendet wird, Einheiten-Suffixe verwendet:
Byte, Kilobyte, Megabyte, Gigabyte, Terabyte und Petabyte, um die
um die Anzahl der Ziffern auf drei oder weniger zu reduzieren und die Basis 2 für Größen zu verwenden.

Jetzt funktioniert `ls -h` nicht mehr alleine. Wenn wir zwei Flags kombinieren wollen,
können wir sie einfach zusammen ausführen. Wenn du also `ls -lh` eingibst und auf
Enter drücken, erhalten wir eine Ausgabe in einem für Menschen lesbaren Format (Achtung: die Reihenfolge spielt hier keine Rolle).

~~~
$ ls -lh
~~~
{: .bash}
~~~
gesamt 0
drwx------+ 6 riley staff 204B Jul 16 11:50 Desktop
drwx------+ 3 riley staff 102B Jul 16 11:30 Dokumente
drwx------+ 3 riley staff 102B Jul 16 11:30 Downloads
drwx------@ 46 riley staff 1.5K Jul 16 11:38 Bibliothek
drwx------+ 3 riley staff 102B Jul 16 11:30 Filme
drwx------+ 3 riley staff 102B Jul 16 11:30 Musik
drwx------+ 3 riley staff 102B Jul 16 11:30 Bilder
drwxr-xr-x+ 5 riley staff 170B Jul 16 11:30 Public
~~~
{: .output}

Wir haben jetzt eine Menge Zeit in unserem Home-Verzeichnis verbracht.
Lass uns woanders hingehen. Das können wir mit dem Befehl `cd` oder Change Directory machen:
(Hinweis: Unter Windows und Mac spielt die Groß-/Kleinschreibung der Datei/des Verzeichnisses standardmäßig keine Rolle.
Unter Linux schon.)

~~~
$ cd Desktop
~~~
{: .bash}

Beachte, dass der Befehl nichts ausgegeben hat. Das bedeutet, dass er erfolgreich ausgeführt wurde.
erfolgreich ausgeführt wurde. Prüfen wir, indem wir `pwd` verwenden:

~~~
$ pwd
~~~
{: .bash}
~~~
/Users/riley/Desktop
~~~
{: .output}

Wenn aber etwas schief gelaufen wäre, hätte der Befehl dir das mitgeteilt. Lass uns
testen wir das, indem wir versuchen, in ein nicht existierendes Verzeichnis zu wechseln:

~~~
$ cd "things to learn about the shell"
~~~
{: .bash}
~~~
bash: cd: Dinge, die man über die Shell lernen kann: No such file or directory
~~~
{: .output}

Beachte, dass wir den Namen in Anführungszeichen gesetzt haben. Die *Argumente*, die man
einem Shell-Befehl angegeben werden, werden durch Leerzeichen getrennt, damit sie wissen, dass
dass wir "eine einzige Sache namens "Dinge, die man über die Shell lernen kann"" meinen und nicht
sechs verschiedene Dinge" meinen, ist, (einfache oder doppelte) Anführungszeichen zu verwenden.

Wir haben jetzt gesehen, wie wir in unserer Verzeichnisstruktur "nach unten" gehen können
(d.h. in weitere verschachtelte Verzeichnisse). Wenn wir zurückgehen wollen, können wir `cd ..` eingeben.
Damit gehen wir ein Verzeichnis nach oben und sind wieder da, wo wir angefangen haben.
**Wenn wir uns einmal verirren, bringt uns der Befehl `cd` ohne Argumente
ohne Argumente direkt in das Heimatverzeichnis zurück, also dorthin, wo wir angefangen haben.**

> ## Vorheriges Verzeichnis
> Um zwischen zwei Verzeichnissen hin und her zu wechseln, verwende `cd -`.
{: .callout}

> ## Probiere es aus
>
> Bewege dich auf dem Computer, gewöhne dich daran, dich in Verzeichnissen zu bewegen und diese zu verlassen,
> Sieh dir an, wie verschiedene Dateitypen in der Unix-Shell erscheinen. Vergewissere dich, dass du die Befehle `pwd` und
> `cd` und die verschiedenen Flags für den Befehl `ls`, die du bisher gelernt hast.
>
> Wenn du mit Windows arbeitest,
> versuche auch `explorer .` einzugeben, um den Explorer für das aktuelle Verzeichnis zu öffnen
> (der einzelne Punkt bedeutet "aktuelles Verzeichnis"). Wenn du mit einem Mac arbeitest,
> versuche es mit `open .` und unter Linux mit `xdg-open .`, um den grafischen Dateimanager zu öffnen.
>
{: .challenge}


Die Fähigkeit, im Dateisystem zu navigieren, ist sehr wichtig, um die Unix-Shell effektiv zu verwenden.
Wenn wir uns damit vertraut machen, können wir sehr schnell zu dem gewünschten Verzeichnis gelangen.

> ## Hilfe bekommen
>
> Verwende den Befehl `man`, um die Handbuchseite (Dokumentation) für einen Shell-Befehl aufzurufen.
> Der Befehl `man ls` zeigt dir zum Beispiel alle Argumente an, die dir zur Verfügung stehen - das erspart
> Du musst sie dir nicht alle merken! Probiere das für jeden Befehl aus, den du bisher gelernt hast.
> Verwende die <kbd>Leertaste</kbd>, um in den Handbuchseiten zu navigieren. Verwende <kbd>q</kbd> jederzeit, um zu beenden.
>
> ***Hinweis*: Dieser Befehl ist nur für Mac- und Linux-Benutzer** gedacht. Er funktioniert nicht direkt für Windows-Benutzer.
> Wenn du Windows verwendest, kannst du auf [http://man.he.net/](http://man.he.net/) nach dem Shell-Befehl suchen,
> und dir die dazugehörige Handbuchseite ansehen. Auf manchen Systemen funktioniert der Befehlsname gefolgt von `--help`, z.B. `ls --help`.
>
> Außerdem listet das Handbuch die Befehle einzeln auf, z.B. obwohl `-h` nur zusammen mit der Option `-l` verwendet werden kann,  
> findest du ihn im Handbuch als `-h` und nicht als `-lh`.
>
> >## Antwort
> >~~~
> >$ man ls
> >~~~
> >{: .bash}
> >~~~
> >LS(1) BSD General Commands Manual LS(1)
> >
> >NAME
> > ls -- Verzeichnisinhalte auflisten
> >
> > >SYNOPSIS
> > ls [-ABCFGHLOPRSTUW@abcdefghiklmnopqrstuwx1] [file ...]
> >
> >BESCHREIBUNG
> > Für jeden Operanden, der eine Datei eines anderen Typs als Verzeichnis benennt, zeigt ls
> > den Namen der Datei sowie alle angeforderten Informationen an.  Für
> > jeden Operanden, der eine Datei vom Typ Verzeichnis benennt, zeigt ls die Namen
> > der in diesem Verzeichnis enthaltenen Dateien sowie alle angeforderten, zugehörigen Informationen an.
> > zugehörigen Informationen an.
> >
> > Wenn keine Operanden angegeben werden, wird der Inhalt des aktuellen Verzeichnisses angezeigt.
> > wiedergegeben.  Wenn mehr als ein Operand angegeben wird, werden die Nicht-Verzeichnis-Operanden
> > werden die Nicht-Verzeichnis-Operanden zuerst angezeigt; Verzeichnis- und Nicht-Verzeichnis-Operanden werden getrennt
> > getrennt und in lexikografischer Reihenfolge.
> >
> > Die folgenden Optionen sind verfügbar:
> >
> > -@ Erweiterte Attributschlüssel und -größen in langer (-l) Ausgabe anzeigen.
> >
> > -1 (Die numerische Ziffer ``Eins''.) Erzwingt eine Ausgabe mit einem Eintrag pro
> > Zeile.  Dies ist die Standardeinstellung, wenn die Ausgabe nicht auf einem Terminal erfolgt.
> >
> > -A Alle Einträge auflisten außer . und ...  Wird immer für den Super- > > Benutzer gesetzt.
> > Benutzer gesetzt.
> >
> >...mehrere weitere Seiten...
> >
> >BUGS
> > Um die Abwärtskompatibilität zu wahren, sind die Beziehungen zwischen den vielen
> > Optionen recht komplex.
> >
> >BSD 19. Mai 2002 BSD
> >
> >~~~
> > {: .output}
> {: .solution}
{: .challenge}


> ## Informiere dich über fortgeschrittene `ls`-Befehle
>
> Finde mithilfe der Manual Page heraus, wie du die Dateien in einem
> Verzeichnis nach ihrer Dateigröße sortiert auflistet. Probiere es in verschiedenen Verzeichnissen aus. Kannst du es kombinieren
> mit dem `-l` *Argument* kombinieren, das du vorher gelernt hast?
>
> Danach,
> finde heraus, wie du eine Liste von Dateien nach dem Datum ihrer letzten Änderung ordnen kannst.
> Versuche, Dateien in verschiedenen Verzeichnissen zu ordnen.
>
> > ## Antwort
> >
> > Um Dateien in einem Verzeichnis nach ihrer Dateigröße zu ordnen, in Kombination mit dem Argument `-l`:
> >
> > ~~~
> > ls -lS
> > ~~~
> > {: .bash}
> >
> > Beachte, dass das "S" **Groß- und Kleinschreibung beachtet!**
> >
> > Um Dateien in einem Verzeichnis nach ihrem letzten Änderungsdatum zu ordnen, in Kombination mit dem Argument "l":
> >
> > ~~~
> > ls -lt
> > ~~~
> > {: .bash}
> {: .solution}
{: .challenge}
