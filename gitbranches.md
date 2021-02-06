Git Branches
============
<br>

Branch (englisch für “Zweig”), stellt ein Abzweiger vom Hauptbranch (main) dar. Wenn du auf deinen Branch Änderungen committest, sind diese unabhängig vom “main” Branch.
Ist man mit der Entwicklung auf dem Branch fertig, so kann man den Branch wieder in den Hauptbranch “main” zurückführen. Diesen Vorgang nennt man “mergen”.

<br>

## **Lokalen Branch erstellen**

--> git branch dateiname

<br>

## **Branch wechseln**

Wenn du den lokalen Branch erstellt hast, befindest du dich weiterhin auf dem vorherigen Branch. Um auf den neu erstellten Branch zu wechseln, musst du einen “checkout” machen.

--> git checkout dateiname
--> git checkout main (Retour zum Hauptzweig)

<br>

## **Branch erstellen und wechseln**

Willst du einen neuen Branch erstellen und direkt auf diesen Branch wechseln, so kannst du dies mit untenstehendem Befehl in einem Schritt durchführen:

--> git checkout -b dateiname

<br>

## **Branch löschen**

--> git branch -d dateiname

<br>

## **Branch veröffentlichen**
--> git push -u origin dateiname

<br>

## **Remote Branch löschen**

Löscht man einen lokalen Branch, so besteht dieser weiterhin auf dem Remote. Dieser kann mit folgendem Befehl auch auf dem Remote gelöscht werden (Git Version 1.7+):

--> git push origin --delete dateiname