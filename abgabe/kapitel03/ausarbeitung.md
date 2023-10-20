# Kapitelüberschrift

**Autor:** Sascha Hahn

## Version control systems / Source code management
Version control Systems (VSC) sind Softwaretools, die Änderungen von Datein/Projekten verwalten und versionieren.
Sie werden auch benutzt um die Zusammenarbeit von mehreren Entwicklern zu ermöglichen und zu erleichtern.
Mit ihnen können zum Beispiel auch Buggs und deren Urpsrung gefunden werden, die Einflüsse der einzelnen Entwickler am Projekt
oder auch alte Teile des Projektes wiederhergestellt werden, von denen man dachte man bräuchte sie nicht mehr.
[1]

### Centralized vs Distributed Version Control
Bei einem zentralisierten VCS gibt es einen zentralen Server, auf dem die Änderungen und Versionsstränge(Repoitory) gespeichert sind. Die Entwickler sind darauf angewiesen immer mit dem Server verbunden zu sein wenn sie eine Änderung machen wollen, da sie nur eine lokale Kopie des Projektes haben(Workingcopy).
Bei einem Distributed VCS hat jeder Entwickler eine kopie des Repositories auf seinem Rechner. Wenn Sie Änderungen machen, dann werden diese in ihrem lokalen Repository gespeichert und später mit dem zentralen Repository synchronisiert.
[2]

### Git
Die meisten werden das VCS Git aus dem letzten Semester kennen. Git ist ein distributed VCS, das von Linus Torvalds entwickelt wurde.

#### Relevanten git-Kommandos und -Workflows
Es gibt grundlegend drei verschiedene Bereiche mit denen man Arbeitet. Das ist die Working Copy/Directory, der Index und das Repository.

**Working Directory:** Sind alle lokalen Datein die im Bereich des Repositories fallen. Ein lokales Repository initialisiert man mit
```bash
git init
```
Alle Dateien in disem Verzeichnis sind jetzt *nur* Teil der Wirking copy

**Stage**: Dateien welche in das Repo mit aufgenommen werde sollen müssen erstmal in den stage Breich verschoben werden.
Dies geschieht mit:
```bash
git add <filename>
git add --all
```
**History/Commit:**
```bash
git commit
```
Mit diesem Befehl werden alle Änderungen der Datein die sich im Stage Bereich befinden in das Repository übernommen. Dadruch ensteht ein "Commit" welcher alle Änderungen zu seinem Vorherigen Commit enthält
<div style="display: flex; align-items: center;">
  <img src="media/GitBasics1.png" alt="Mein Bild" style="width: 500px; height: auto;">
  <p>
  eine typische Abfolge an Befehlen wäre z.B:<br> <br>
    git add ausrbeitung.md <br>
    git add GitBasics.png <br>
    git commit -m "added chapter 3" <br>
</div>

[1,3]

#### Remote repositories
Remote repositories sind jene, mit denen sich alle Entwickler Synchronisieren. Entwickler machen änderungen in ihrem lokalen repository und synchronisieren ihre änderungen dann später mit dem remote.
Wenn ein entwickler neue commits erstellt, muss der urpsrüngliche commit auch auf dem remote vorhanden sein, damit die änderungen übernommen werden können.
```bash
git push
```
##### Branches
Damit Entwickler ungestört an ihren änderungen arbeiten können, ohne die arbeit der anderen zu beeinflussen, werden branches benutzt. Jeder Entwickler hat seinen eigenen Branch der seine Änderungen enthält. Diese Branches können auch auf dem remote als einzelne Branches gepusht werden, so das andere Entwickler auf diese zugreifen können.
Wenn ein Entwickler mit seinen Änderungen fertig ist, kann er diese in den main Branch mergen. Dieser ist der Hauptbranch, der alle Änderungen enthält.
```bash
git switch -c <branchname>
git push -u origin <branchname>

git switch main
git merge <branchname>
```
[1]




#### Multirepos vs. Monorepos
**Multirepo:** Jedes Projekt/Teile eines Projektes werden in einzelnen Repos Versioniert
**Monorepo:** Alle Projekte/Teile eines Projektes werden in einem Repo Versioniert

|      |Pro          |Con         |
|:-:   |:----------|:-----------|
|Multi| Reduziet unerwünschte Abhängigkeiten|Hinzufgügen von Abhängigkeiten schwieriger|
||Teams können unabhängiger an Teilen Arbeiten|Teilen von Code/Resourcen zwischen Projekten umständlicher|
||Einfachere Verwaltung und Skalierbarkeit durch Übersichtlichkeit einfacher|Keine Einheitliche Versionskontrolle(welche Version des einen Projekts ins kompatibel mit dem Anderen?)|
|Mono|Einfache Abhängigkeiten|Verwaltung und allgemeine Arbeit ist schwieriger, druch unübersichtlichkeit|
||Konsistente Versionskontrolle|Entwickler Teams behindern sich häufiger|
||einfache ResourcenTeilung||

**kleines Fazit:**<br>
Multirepos sind für kleinere Projekte besser geeignet, da sie einfacher zu verwalten sind. Bei größeren Projekten ist ein Monorepo besser geeignet, da es die Übersichtlichkeit erhöht und die Abhängigkeiten einfacher zu verwalten sind.
[4]

#### Submodules
Submodules sind Repositories die in einem anderen Repository liegen. Sie werden benutzt um Code/Resourcen zwischen Projekten zu teilen, wie z.B. eine Bibliothek.
Man kann sie mit dem folgendem Befehl hinzufügen:
```bash
git add submodule <url>
```
Dabei erstellt git einen Ordner mit dem Namen des Submodules und eine Datei namens *.gitmodules* in dem der pfad und die url aller submodules gespeichert werden.

[5]
#### Pull Requests
Pull Request sind ein Teil der Plattform Git-Hub.
Git-Hub ist ein unbhängiger anbieter von Git, der es ermöglicht Projekte auf einem Server zu hosten und mit anderen Entwicklern zu teilen.

Bei einem Pull request stellt ein Entwickler seine Änderungen anderen Entwicklern zur verfügung. Diese können dann die Änderungen übernehmen oder ablehnen.
Der Entwickler hat also einen eigenen Branch erstellt, auf diesem änderungen gemacht und stellt jetzt eine anfrage zum mergen dieses branches in den main branch.
[1]

#### Branching strategies
Branching strategien sind Arbeitsweisen mit denen festfelegt wurde wie mit branches umgegangen wird und wie man das Projekt dmit sturkturiert.

##### Long-lived branches
Im Allgemeinen gibt es zwei Arten von Branches. Long-lived und Short-lived branches. Long-Lied Branches sind, jene die über einen längeren Zeitraum bestehen bleiben, wie zum Beispiel ein Release oder Version Branch.
[2]

##### Trunk-based Development
Dies ist die wohl einfachste Variante der Branching strategien. Es gibt nur einen Branch, den main branch. Alle Entwickler arbeiten auf diesem Branch und commiten ihre Änderungen direkt auf diesen Branch.
Man kann aber auch auf anderen Branches Arbeiten und diese dann in den main Branch mergen und rebasen.
[2]

##### Git Flow
Git Flow ist eine Branching strategie die von Vincent Driessen entwickelt wurde. Die besteht aus 3 verschiedenen Long Lived Branches und mindestens 2 Short Lived Branches.
###### Feature, develop, release, hotfix und main branch
![](media/GitFlow.png)

**Develop:** Ist der Hauptbranch von dem alle anderen Branches abzweigen. Auf dem Hauptbranch direkt werden aber nur kleinere Bugfixes gemacht oder ähnliches gemacht.

**Feature:** Feature Branches entspringen aus dem Develop Branch und werden benutzt um neue Features zu entwickeln. Wenn ein Feature fertig ist, wird es in den Develop Branch gemerged. Es kann beliegbig viele Feature Branches geben.

**Release:** Release Branches werden benutzt um ein Release vorzubereiten. Auf diesem Branch werden nur noch letzte Bugfixes gemacht und andere für den Release wichtige Sachen fertigestellt. Der Vorteil an dem Release Branch ist, dass man auf dem Develop schon für den nächsten Release weiter arbeiten kann. Alle Änderungen die auf dem Release Branch gemacht werden, werden auch in den Develop Branch gemerged und in den Main Branch gemerged, wenn der Release fertig ist.

**Main:** Auf der Main Branch werden alle fertigen Releases festgehalten. Jeder Release wird mit einem Tag versehen, der die Versionsnummer enthält.

**Hotfix:** Bei schwerwiegenden Bugs die es in einen Release geschafft haben, wird ein Hotfix Branch erstellt. Auf diesem Branch werden die Bugs gefixt und direkt wieder in den Main und Develop Branch gemerged. Der neue commit auf dem Main branch bekommt auch wieder einen Tag mit der neuen Versionsnummer.
[1]

##### Github Flow
Bei dem Github Flow gibt es nur einen long-lived Branch, den Main Branch. Bei Features oder Bugfixes werden weitere kurzlebige Feature Branches erstellt, welche dann später in den main gemerged werden.
Die besonderheit beim Github Flow ist jetzt, dass die Entwickler einen Merge-Request auf GitHub stellen. Der Merge-Request wird dann von anderen Entwicklern geprüft, diskutiert und dann automatisch in den main gemerged.

[1]
#### Merging strategies
Es gibt verscheidenen Möglichkeiten Branches zu vereinigen:

##### Merge Commit
```bash
git switch main
git merge <branchname>
```
Hier wird ein neuer Commit erzeigt, welcher die Änderungen der beiden Branches zusammenführt. Wenn nur einer der beiden neuen Branches Änderungen enthält, dann geschieht ein *fast-forward*. Beide Branches zeigen dann auf den selben Commit und es wird kein neuer erstellt.
Es kann auch ein bestimmtes verhalten geforced werden mit den Parametern *--no-ff* und *--ff-only*.
[1]

##### Squash and Merge
```bash
git switch main
git merge --squash <branchname>
```
Alle commits des Branches werden zu einem zusammengefasst und dann in den main Branch gemerged.
[1]
##### Rebase and Merge
#### Aufbau und Inhalt von Commit messages
      * https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53
## AI-driven development
### Conversational AI vs. Generative AI
### Prompt engineering
### ChatGPT, Github Copilot
### Best practices für "googling"

## Referenzen

[1] :**Carsen Gips, Programmiermethoden Script:** https://www.hsbi.de/elearning/data/FH-Bielefeld/lm_data/lm_1359639/index.html
[2] :https://chat.openai.com/
[3] :https://marklodato.github.io/visual-git-guide/index-en.html
[4] :https://kinsta.com/blog/monorepo-vs-multi-repo/
[5] :https://git-scm.com/book/en/v2/Git-Tools-Submodules