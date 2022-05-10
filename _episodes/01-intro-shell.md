---
Titel: "Was ist die Shell?"
Unterricht: 5
Übungen: 0
Fragen:
- "Was ist die Shell?"
- "Was ist die Kommandozeile?"
- "Warum sollte ich sie verwenden?"
Ziele:
- "Beschreibe die Grundlagen der Unix-Shell"
- "Erkläre, warum und wie du die Kommandozeile verwendest"
Kernpunkte:
- "Die Shell ist mächtig"
- "Die Shell kann zum Kopieren, Verschieben und Kombinieren mehrerer Dateien verwendet werden"
---

## Einleitung: Was ist die Shell, und warum sollte ich sie benutzen?
Wenn Sie schon einmal mit großen Datenmengen oder einer großen Anzahl digitaler Dateien zu tun hatten, die über Ihren Computer oder einen entfernten Server verstreut sind, wissen Sie, dass das Kopieren, Verschieben, Umbenennen, Zählen, Durchsuchen oder sonstige manuelle Bearbeitung dieser Dateien immens zeitaufwändig und fehleranfällig sein kann. Glücklicherweise gibt es ein außergewöhnlich leistungsstarkes und flexibles Werkzeug, das genau für diesen Zweck entwickelt wurde.

Die Shell (manchmal auch als "Unix-Shell" bezeichnet, für das Betriebssystem, für das sie ursprünglich entwickelt wurde) ist ein Programm, das es Ihnen erlaubt, mit Ihrem Computer über eingetippte Textbefehle zu interagieren. Sie ist die primäre Schnittstelle, die auf Linux- und Unix-basierten Systemen, wie z.B. MacOS, verwendet wird, und kann optional auf anderen Betriebssystemen, wie z.B. Windows, installiert werden.

Es ist das definitive Beispiel einer "Befehlszeilenschnittstelle", bei der dem Computer durch die Eingabe von Befehlen Befehle gegeben werden und der Computer darauf mit der Ausführung einer Aufgabe oder der Erzeugung einer Ausgabe antwortet. Diese Ausgabe wird oft auf den Bildschirm gelenkt, kann aber auch auf eine Datei oder sogar auf andere Befehle gelenkt werden, so dass mit sehr geringem Aufwand leistungsfähige Aktionsketten entstehen.

Die Verwendung einer Shell fühlt sich manchmal eher wie Programmieren als wie die Verwendung einer Maus an. Befehle sind prägnant (oft nur ein paar Zeichen lang), ihre Namen sind häufig kryptisch, und ihre Ausgabe besteht aus Textzeilen und nicht aus etwas Visuellem wie einem Graphen. Auf der anderen Seite erlaubt die Shell mit nur wenigen Tastenanschlägen, vorhandene Werkzeuge zu leistungsfähigen Pipelines zu kombinieren und große Datenmengen automatisch zu verarbeiten. Diese Automatisierung macht Sie nicht nur produktiver, sondern verbessert auch die Reproduzierbarkeit Ihrer Arbeitsabläufe, da Sie diese mit wenigen einfachen Befehlen speichern und dann wiederholen können. Das Verständnis der Grundlagen der Shell bietet eine nützliche Grundlage für das Erlernen des Programmierens, da sich einige der Konzepte, die Sie hier lernen werden - wie Schleifen, Werte und Variablen - auf die Programmierung übertragen lassen.

Die Shell ist eine der produktivsten Programmierumgebungen, die je geschaffen wurden. Wenn Sie sie einmal beherrschen, können Sie mit ihr interaktiv mit verschiedenen Befehlen experimentieren und dann das Gelernte zur Automatisierung Ihrer Arbeit verwenden.

In dieser Sitzung werden wir in die Aufgabenautomatisierung einführen, indem wir uns ansehen, wie Daten mit Hilfe der Shell manipuliert, gezählt und abgebaut werden können. Die Sitzung wird eine kleine Anzahl von Basisbefehlen behandeln, die Bausteine darstellen, auf denen komplexere Befehle konstruiert werden können, die zu Ihren Daten oder Ihrem Projekt passen. Auch wenn Sie nicht selbst programmieren oder Ihre Arbeit derzeit nicht die Befehlszeile umfasst, kann es nützlich sein, einige Grundlagen über die Shell zu kennen.

Anmerkung für den Lektionsausbilder: Erwägen Sie, hier ein Beispiel dafür zu geben, wie Sie in der letzten Woche oder im letzten Monat die Unix-Shell zur Lösung eines Problems verwendet haben

## Wo ist meine Shell?
Die Shell ist ein Programm, das normalerweise auf Ihrem Computer gestartet wird, ähnlich wie Sie jedes andere Programm starten würden. Es gibt jedoch zahlreiche Arten von Shells mit unterschiedlichen Namen, und sie können bereits installiert sein oder auch nicht. Die Shell ist das Herzstück von Linux-basierten Computern, und macOS-Maschinen werden mit Terminal, einem Shell-Programm, ausgeliefert. Für Windows-Benutzer bieten populäre Shells wie Cygwin oder Git Bash eine Unix-ähnliche Oberfläche, müssen aber möglicherweise separat installiert werden. In Windows 10 bietet die PowerShell diese Funktionalität von Haus aus.

In dieser Lektion werden wir Git Bash für Windows-Benutzer, Terminal für MacOS und die Shell für Linux-Benutzer verwenden.

