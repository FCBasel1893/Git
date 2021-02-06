Mein erstes Repository
======================

--> `mkdir` Ordner erstellen

--> `cd` in den Ordner wechseln

--> `git init` Projekt erstellen

<br>

## Main vs Master
`git config --global init.defaultBranch main/master`

(muss nur einmal gemacht werden)

<br>

## Datei hinzufügen (stagen)
Neue Dateien im Ordner erstellen

z.B. index.html / main.js / styles.css usw. --> `nano . index.html`

--> git status

--> git add index.html (Datei erscheint im Terminal **rot**)

--> git status (Datei erscheint im Terminal **grün**)

<br>

## Datei entfernen (unstagen)
--> git reset -- index.html

--> git rm --cached index.html

--> git status (Datei erscheint im Terminal **rot**)

<br>

## Änderungen “committen"
--> git commit -m "add index.html"
--> git status
--> git log

<br>

## Datei "pushen"
--> git push

<br>

## Repository auf Github erstellen
--> New repository

--> repository Name geben --> create repository

<br>

## Remote hinzufügen

--> ...or push an existing repository from the command line

git remote add origin https://github.com/benutzername github/ordnername.git

<br>

## Remote hinzufügen
--> git remote add origin git@githubcom:`FCBasel1893`/`Dateiname`.git

--> git push -u origin `main/master` 

### **Nun ist die Datei auf Github**

<br>

## .gitignore

Datei in VSC erstellen mit dem Namen .gitignore

Inhalt

.idea
.DS_Store
/dist

<br>

## .gitkeep (inoffiziell)
Git ist nicht in der Lage, leere Verzeichnisse in die Versionsverwaltung aufzunehmen. Möchte man für ein Projekt "leere" Verzeichnisse anlegen (z.B. für Bilder, so kann man darin eine leere Datei mit dem Namen .gitkeep erstellen)

<br>

## Initiales Setup

Muss nur einmal pro Computer gemacht werden.

--> git config --global user.email "fabian.s.ftp@gmail.com"
--> git config --global user.name "Fabian Schuoler"

<br>

## SSH Key Authentifizierung mit Github

*Prüfen, ob bereits ein SSH Key existiert*

1. Terminal öffnen
2. Kommando --> ls -la ~/.ssh eintippen
3. Ausgabe auf bereits vorhandene *.pub Dateien untersuchen

<br>

*Folgende Dateien deuten auf ein bereits vorhandenen Key hin:*

* id_dsa.pub
* id_ecdsa.pub
* id_ed25519.pub
* id_rsa.pub

<br>

**Falls keine *.pub Datei vorhanden ist, muss ein neuer Key erzeugt werden:**

1. Terminal öffnen
2. Kommando `ssh-keygen -t rsa -b 4096 -c "fabian.s.ftp@gmail.com"`
3. Enter a file in which to save the key (/Users/you/.ssh/id_rsa):--> Enter drücken
4. Enter passphrase (empty for no passphrase); **[Passwort eingeben]**
Enter same passphrase again: **[Passwort erneut eingeben]**

<br>

*Der Public Key muss nun bei Github hinterlegt werden (Beispiel mit Key namens id_rsa.pub)*

1. Browser öffnen und `https://github.com/settings/keys` aufrufen
2. Terminal öffnen
3. Kommando `cat ~/.ssh/id_rsa.pub` eintippen und key Kopieren
4. "New SSH key" anklicken
5. Key einfügen und mit "Add SSH key" speichern


===================================================================
