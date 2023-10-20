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
Remote repositories sind jene, mit denen sich alle Entwickler Synchronisieren.

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
#### Pull requests
#### Branching strategies
      * https://mermaid.js.org/syntax/gitgraph.html
##### Trunk-based Development
##### Long-lived branches
##### Git Flow
###### Feature, develop, release, hotfix und master branch
##### Github Flow
#### Merging strategies
##### Merge Commit
##### Squash and Merge
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