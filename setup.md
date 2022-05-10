---
Layout: Seite
Titel: Einrichtung
---

Um an dieser Library Carpentry-Lesson teilnehmen zu können, benötigst du eine funktionierende UNIX-ähnliche Shell-Umgebung.
Konkret werden wir Bash ([Bourne Again Shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell))) verwenden, die unter Linux und macOS Standard ist. macOS Catalina-User haben zsh (Z-Shell) als Standardversion.
Auch wenn du ein Windows-User bist, eröffnet dir das Erlernen der Bash eine Reihe von mächtigen Werkzeugen auf deinem persönlichen Rechner und macht dich außerdem mit der Standard-Fernbedienungsschnittstelle vertraut, die auf fast allen Servern und Supercomputern verwendet wird.

>## Terminal-Einrichtung
>
>Bash ist die Standardshell der meisten Linux-Distributionen und von macOS.
>Windows-User benötigen Git Bash, um eine UNIX-ähnliche Umgebung zu erhalten.
>
>- **Linux:** Die Standard-Shell ist normalerweise Bash, aber wenn dein Rechner anders eingerichtet ist, kannst du sie starten, indem du ein Terminal öffnest >und `bash` eingibst.  Du brauchst nichts zu installieren. Such in deinen Anwendungen nach Terminal, um die Bash-Shell zu starten.
>- **macOS:** Bash ist die Standard-Shell in allen Versionen von macOS vor Catalina, du brauchst nichts zu installieren. Öffnen Sie Terminal über >`/Anwendungen/Dienstprogramme` oder die Spotlight-Suche, um die Bash-Shell zu starten. zsh ist die Standardeinstellung in Catalina.
>- **Windows:** Unter Windows sind normalerweise CMD oder PowerShell als Standard-Shell-Umgebungen verfügbar. Diese verwenden eine Syntax und eine Reihe von Anwendungen, die es nur auf Windows-Systemen gibt, und sind nicht mit den weiter verbreiteten UNIX-Dienstprogrammen kompatibel. Es kann jedoch eine Bash-Shell unter Windows installiert werden, um eine UNIX-ähnliche Umgebung zu schaffen. Für diese Lesson schlagen wir vor, Git Bash zu verwenden, das Teil des Pakets >[Git für Windows](https://gitforwindows.org/) ist:
> - Lade das neueste [Installationsprogramm] für Git für Windows herunter (https://gitforwindows.org/).
> - Doppelklicke auf die `.exe`, um das Installationsprogramm (z. B. `Git-2.13.3-64-bit.exe`) unter Verwendung der Standardeinstellungen auszuführen.
> - Nach der Installation öffnest du die Shell, indem du Git Bash aus dem Startmenü (im Git-Ordner) auswählst.
>
> Es gibt auch einige fortgeschrittenere Lösungen für die Ausführung von Bash
> Befehle unter Windows.  Ein Bash-Shell-Befehlszeilentool ist für > Windows 10 verfügbar.
> Windows 10, das du verwenden kannst, wenn du das [Windows Subsystem für
> Linux] (https://docs.microsoft.com/en-us/windows/wsl/install-win10) aktivieren.
> Außerdem kannst du Bash-Befehle auf einem entfernten Computer oder Server ausführen
> der bereits eine Unix-Shell hat, von deinem Windows-Rechner aus ausführen.  Dies kann
Dies kann > normalerweise über einen Secure Shell (SSH)-Client erfolgen.  Ein solcher Client
> kostenlos für Windows-Computer erhältlich ist
> [PuTTY](https://www.putty.org/).
>
>Wenn du auf Probleme stößt, unterhält Carpentries eine [Configuration Problems and Solutions wiki page](https://github.com/carpentries/workshop-template/wiki/Configuration-Problems-and-Solutions), die dir helfen kann.
{: .prereq}

>## Datendateien
>
>Du benötigst einige Dateien, um dieser Lesson zu folgen:
>
>1. Lade [shell-lesson.zip]({{ page.root }}/data/shell-lesson.zip) herunter und verschiebe die Datei auf deinen Desktop.
>2. Entpacke / extrahiere die Datei (frage deinen Instructor, wenn du Hilfe bei diesem Schritt benötigst). Du solltest nun einen neuen Ordner mit dem Namen "shell-lesson" auf deinem Desktop haben.
>3. Öffne das Terminal und gib `ls` gefolgt von der <kbd>Enter</kbd> Taste ein.
>~~~~
>$ ls
>~~~~
>{: .bash}
> Du solltest eine Liste von Dateien und Ordnern in deinem aktuellen Verzeichnis sehen.
>4. Dann tippe:
>
>~~~
>$ pwd
~~~~
>{: .bash}
> Dieser Befehl zeigt dir, wo du dich in deinem Dateisystem befindest, was jetzt dein Home-Verzeichnis sein sollte. In der Lesson erfährst du mehr über die Befehle `ls`, `pwd` und wie du mit den Daten im Ordner `shell-lesson` arbeiten kannst.
{: .prereq}

[template]: {{ site.workshop_repo }}
