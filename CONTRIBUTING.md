# Mitwirken

Die [Carpentries][c-site] ([Software Carpentry][swc-site], [Data Carpentry][dc-site] und [Library Carpentry][lc-site]) sind Open Source Projekte,
und wir begrüßen Beiträge aller Art:
neue Lessons,
Korrekturen an bestehendem Material,
Fehlerberichte,
und Bewertungen von vorgeschlagenen Änderungen sind willkommen.

## Mitwirkende Vereinbarung

Wenn Sie mitwirken,
stimmen Sie zu, dass wir Ihre Arbeit unter [unserer Lizenz] (LICENSE.md) weitergeben dürfen.
Im Gegenzug,
werden wir auf Ihre Probleme eingehen und/oder Ihren Änderungsvorschlag so schnell wie wir können bewerten,
und Ihnen helfen, ein Mitglied unserer Gemeinschaft zu werden.
Jeder, der an [The Carpentries][c-site]
erklärt sich damit einverstanden, sich an unseren [Verhaltenskodex](CODE_OF_CONDUCT.md) zu halten.

## Wie man mitwirkt

Der einfachste Weg ist, einen Fehler zu melden
um uns über einen Rechtschreibfehler zu informieren,
eine unglückliche Formulierung,
oder einen sachlichen Fehler.
Dies ist eine gute Möglichkeit, sich vorzustellen
und einige unserer Community-Mitglieder kennenzulernen.

1.  Wenn du kein [GitHub][github]-Konto hast,
kannst du [uns Kommentare per E-Mail][E-Mail] schicken.
    Wie auch immer,
wir können jedoch schneller reagieren, wenn du eine der anderen unten beschriebenen Methoden verwendest.

2.  Wenn du ein [GitHub][github]-Konto hast,
oder bereit bist, eines zu [erstellen][github-join],
aber nicht weißt, wie man Git verwendet,
kannst du Probleme melden oder Verbesserungen vorschlagen, indem du ein [issue][issues] erstellst.
    Dadurch können wir das Problem jemandem zuweisen
    zuzuordnen und in einem Diskussionsstrang darauf zu antworten.

3.  Wenn du mit Git vertraut bist,
und Material hinzufügen oder ändern möchtest,
kannst du einen Pull Request (PR) einreichen.
Eine Anleitung dazu findest du [unten](#using-github).

## Wo du mitwirken kannst

1.  Wenn du diese Lesson ändern möchtest,
arbeite bitte in <https://github.com/swcarpentry/FIXME>,
    das unter <https://swcarpentry.github.io/FIXME> eingesehen werden kann.

2.  Wenn du die Beispiellektion ändern möchtest,
arbeite bitte in <https://github.com/carpentries/lesson-example>,
    die das Format unserer Lesson dokumentiert
    und kann unter <https://carpentries.github.io/lesson-example> eingesehen werden.

3.  Wenn du die für die Workshop-Webseiten verwendete Vorlage ändern möchtest,
arbeite bitte in <https://github.com/carpentries/workshop-template>.
    Auf der Startseite dieses Repositorys wird erklärt, wie man Workshop-Websites einrichtet,
    während die zusätzlichen Seiten in <https://carpentries.github.io/workshop-template>
    bieten mehr Hintergrundinformationen zu unseren Designentscheidungen.

4.  Wenn du CSS-Stildateien, Tools,
    oder HTML-Vorlagen für Lessons oder Workshops, die in `_includes` oder `_layouts` gespeichert sind,
arbeite bitte in <https://github.com/carpentries/styles>.

## Woran man mitwirken kann

Es gibt viele Möglichkeiten, mitzuwirken,
vom Schreiben neuer Übungen und der Verbesserung bestehender Übungen
zum Aktualisieren oder Ergänzen der Dokumentation
und dem Einreichen von [Fehlerberichten][Problemen]
über Dinge, die nicht funktionieren, unklar sind oder fehlen.
Wenn du nach Ideen suchst, schaue bitte auf die Registerkarte 'Issues' für
eine Liste der mit diesem Repository verbundenen Probleme,
oder du kannst auch in den Problemen für [Data Carpentry][dc-issues] suchen, 
[Software Carpentry][swc-issues], und [Library Carpentry][lc-issues] ansehen.

Kommentare zu Issues und Reviews von Pull Requests sind ebenso willkommen:
Gemeinsam sind wir schlauer als allein.
Bewertungen von Anfängern und Neulingen sind besonders wertvoll:
Leute, die diese Lessons schon eine Weile verwenden, vergessen leicht
vergessen, wie undurchdringlich manches von diesem Material sein kann,
Daher sind frische Augen immer willkommen.

## Woran man *nicht* mitwirken sollte

Unsere Lessons enthalten bereits mehr Material, als wir in einem typischen Workshop behandeln können,
Daher suchen wir normalerweise *nicht* nach weiteren Konzepten oder Werkzeugen, die wir hinzufügen können.
In der Regel,
wenn du eine neue Idee einbringen willst,
musst du (a) abschätzen, wie lange es dauern wird, dich zu unterrichten
und (b) erklären, was du herausnehmen würdest, um Platz dafür zu schaffen.
Der erste Punkt ermutigt die Mitwirkenden, die Anforderungen ehrlich zu formulieren;
die zweite dazu, sich Gedanken über Prioritäten zu machen.

Wir suchen auch nicht nach Übungen oder anderem Material, das nur auf einer Plattform läuft.
Unsere Workshops bestehen in der Regel aus einer Mischung von Windows-, macOS- und Linux-Nutzern;
um brauchbar zu sein,
müssen unsere Lessons auf allen drei Plattformen gleich gut laufen.

## GitHub verwenden

Wenn du über GitHub mitwirken möchtest, solltest du Folgendes aufsuchen
[Wie man an einem Open-Source-Projekt auf GitHub mitwirkt][how-contribute].
Um Änderungen zu verwalten, folgen wir dem [GitHub-flow][github-flow].
Jede Lesson hat mindestens zwei Betreuer, die Probleme und Pull Requests überprüfen oder andere dazu ermutigen, dies zu tun.
Die Betreuer sind Freiwillige aus der Gemeinschaft und haben das letzte Wort darüber, was in die Lesson eingefügt wird.
Verwende das Webinterface, um an einer Lesson mitzuwirken:

1.  Forke das ursprüngliche Repository in dein GitHub-Profil.
2.  Wechsle innerhalb deiner Version des geforkten Repositorys in den Zweig "gh-pages" und
erstelle einen neuen Zweig für jede wichtige Änderung.
3.  Navigiere zu der/den Datei(en), die du in den neuen Zweigen ändern möchtest, und nimm die erforderlichen Änderungen vor.
4.  Übertrage alle geänderten Dateien in die entsprechenden Zweige.
5.  Erstelle einzelne Pull Requests von jedem deiner geänderten Zweige
an den Zweig "gh-pages" im ursprünglichen Repository.
6.  Wenn du eine Rückmeldung erhältst, nimmst du die Änderungen in den themenspezifischen Zweigen des geforkten
Repository vor und die Pull Requests werden automatisch aktualisiert.
7.  Wiederhole den Vorgang nach Bedarf, bis alle Rückmeldungen bearbeitet wurden.

Wenn du mit der Arbeit beginnst, vergewissere dich bitte, dass dein Klon des ursprünglichen `gh-pages`-Zweigs aktuell ist
bevor du von dort aus deine eigene(n) revisionsspezifische(n) Verzweigung(en) erstellst.
Außerdem solltest du nur von deinem neu erstellten Zweig aus arbeiten und *nicht* von deinem
deinem Klon des ursprünglichen "gh-pages"-Zweigs.
Schließlich sind die veröffentlichten Kopien aller Lessons im Zweig "gh-pages" des ursprünglichen
Repository zur Verfügung, damit du bei der Überarbeitung nachschlagen kannst.

## Andere Ressourcen

Allgemeine Diskussionen über [Software Carpentry][swc-site], [Data Carpentry][dc-site] und [Library Carpentry][lc-site]
findet auf der [Diskussions-Mailingliste][discuss-list] statt,
auf der jeder willkommen ist.
Du kannst uns auch [per E-Mail][email] erreichen.

[email]: mailto:team@carpentries.org
[dc-issues]: https://github.com/issues?q=user%3Adatacarpentry
[dc-lessons]: http://datacarpentry.org/lessons/
[dc-site]: http://datacarpentry.org/
[discuss-list]: https://carpentries.topicbox.com/groups/discuss
[github]: https://github.com
[github-flow]: https://guides.github.com/introduction/flow/
[github-join]: https://github.com/join
[how-contribute]: https://app.egghead.io/playlists/how-to-contribute-to-an-open-source-project-on-github
[issues]: https://guides.github.com/features/issues/
[swc-issues]: https://github.com/issues?q=user%3Aswcarpentry
[swc-lektionen]: https://software-carpentry.org/lessons/
[swc-site]: https://software-carpentry.org/
[c-site]: https://carpentries.org/
[lc-site]: https://librarycarpentry.org/
[lc-issues]: https://github.com/issues?q=user%3Alibrarycarpentry
