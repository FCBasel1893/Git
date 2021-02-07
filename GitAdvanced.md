Git Befehlsaufbau
=================

**Git aufrufen** 

**git** *add* `test.txt`

<br>

*Was git uns tun soll*
* add
* commit
* reset
* checkout
* push
* pull
* remote

`Parameter, je nach Befehl unterschiedlich`

<br>

## Git Befehlsaufbau

**git** *remote* add origin `<url>`

<br>

**git** = git aufrufen

*remote = Was git uns tun soll*
* add
* commit
* reset
* checkout
* push
* pull
* remote

<br>

add = Unter-Befehl hier für "remote"

origin = frei wählbares Alias für Remote Repository

`<url> Repository URL`


<br>


## Git log (--pretty)

--> git log --pretty-oneline

<br>

## Git log (--author)
--> git log --author=pascal

<br>

## Git log (--graph)

--> git log --graph --oneline --decorate --all

<br>

## Git stash
--> git stash (last in)

--> git stash pop (first out)

<br>

## Git stash apply
--> git stash apply (Datei ist modifiziert/modified --> rot)

<br>

## Git stash pop
--> git stash pop (Datei ist modifiziert/modified --> rot)

<br>

## Git diff
--> git status (on branch/Zweig main)

--> git diff (hier sieht man die Änderungen/Korrekturen, 

welche in der Datei vorgenommen)

<br>

## Datei zurücksetzen
--> git checkout -- dateiname

Setzt die einzelne Datei auf den zuletzt committeten Stand zurück.

<br>

## Alles zurücksetzen
--> git reset --hard HEAD (Setzt die Working Copy auf den zuletzt committeten Stand (genannt HEAD) zurück)

--> git fetch origin

<br>

--> git reset --hard origin/main

Setzt die lokalen Änderungen auf den letzten Stand von Remote "origin" vom Branch/Zweig "main" zurück.

<br>

## Wie lösche ich eine Datei in git

*Variante 1: einfach löschen*
--> git rm dateiname

oder

--> git commit -m "removed test.txt"


<br>

## Git mouve (mv)

--> git mv test.txt test2.txt

Bennennt eine Datei um. Der erste Parameter ist die Ursprungsdatei, 

der zweite Parameter die Zieldatei.

<br>

--> git mv test.txt src/test.txt

Verschiebt die Datei ins Verzeichnis "src". Der erste Parameter ist die Ursprungsdatei, der zweite Parameter die Zieldatei. Gleichzeitig könnte die datei natürlich auch umbenannt werden.

<br>

## Git fetch

--> git fetch [remote-name]

Lädt die aktuellsten Infos (History, Branches usw.) von Remote herunter, so dass diese lokal sichtbar sind.

Die veränderten Dateien werden damit allerdings nicht von Remote heruntergleaden.

--> git log --all

<br>

## git pull

--> git pull

Wenn du nach dem `git fetch` den pull Befehl ausführst, wird Git die neuen Commits aus dem externen Repository holen und versuchen, sie automatisch mit dem Code zusammen zu führen, an dem du gerade arbeitest.


<br>

## git log Pro Mode

--> git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit

<br>

## Alias verwenden

--> git lg


<br>

## Git log Änderungen anzeigen

--> git lg -p


<br>

## Git branch

**Lokalen Branch erstellen**

--> git branch test (Name vom Branch/Zweig)

<br>

## Branch wechseln


--> git branch checkout test (Name vom Branch/Zweig)

<br>

## Branch erstellen und wechseln


--> git checkout -b test (Name vom Branch/Zweig)


<br>

## Branches auflisten

**Lokale Branches anzeigen**


--> git branch

<br>

Ausgabe: 

main

*test


<br>

## Branch löschen

**Unbenutzte oder gemergte Branches sollte man wieder löschen.**


--> git branch -d test (Name vom Branch/Zweig)


<br>

## Branch veröffentlichen


--> git push -u origin BRANCH-NAME



<br>

## Remote Branch löschen

**Mit folgendem Befehl kann dieser aus dem Remote gelöscht werden:**


--> git push origin --delete test (Name vom Branch/Zweig)


<br>

## Was ist mergen?


Mergen (englich für "verschmelzen" bezeihnet den Vorgang, bei dem man den Inhalt aus 2 Dateien (in unserem Fall zwei verschiedene Commits oder Branches) in einer einzigen Datei zusammen führt).

<br>

## Mergen (happy case => no conflicts)


--> git checkout main

--> git merge test


<br>

## Merge abbrechen


--> git merge --abort




