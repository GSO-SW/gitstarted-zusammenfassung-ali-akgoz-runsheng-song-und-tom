
# Git Anleitung

## Fachbegriffe

- **Repository**: Ein Verzeichnis, das alle Projektdateien sowie die vollständige Versionsgeschichte enthält.
- **Commit**: Ein Schnappschuss des aktuellen Projektstands. Jeder Commit enthält eine Nachricht, die die Änderungen beschreibt.
- **Branch**: Ein unabhängiger Entwicklungszweig. Nützlich, um neue Features zu entwickeln, ohne den Hauptzweig zu beeinflussen.
- **Merge**: Der Vorgang, durch den Änderungen aus einem Branch in einen anderen integriert werden.
- **Pull Request**: Ein Vorschlag zur Übernahme von Änderungen, oft mit Review durch andere.
- **Remote**: Ein externes Repository, z. B. auf GitHub.
- **Clone**: Lokales Kopieren eines Remote-Repositories.
- **Push**: Überträgt lokale Commits auf das Remote-Repository.
- **Pull**: Holt Änderungen vom Remote-Repository und integriert sie lokal.


## Git-Befehle – **lokale Arbeit**

Diese Befehle werden verwendet, wenn man lokal (auf dem eigenen Rechner) mit Git arbeitet:

```bash
git init                    # Neues lokales Git-Repository erstellen
git status                 # Zeigt den aktuellen Status der Arbeitsverzeichnisse
git add .                  # Stellt alle Dateien zur Aufnahme bereit
git commit -m "Nachricht"  # Änderungen speichern mit Kommentar
git log                    # Zeigt den Verlauf der Commits an
git merge <branch>         # Merge eines Branches in den aktuellen
git merge --abort          # Merge-Konflikt abbrechen
```

Hinweis: Nutzt `git status`, um Fehler wie ungestagte Dateien zu vermeiden. Vor dem Commit immer `git add` verwenden.



## Befehle – Entfernte Arbeit

- `git clone <url>`: Klont ein Remote-Repository.
- `git remote -v`: Zeigt die verbundenen Remotes an.
- `git fetch`: Holt Änderungen vom Remote, integriert sie aber nicht.
- `git pull`: Holt und integriert Remote-Änderungen.
- `git push`: Überträgt lokale Änderungen ins Remote-Repository.
- `git branch -r`: Zeigt entfernte Branches an.
- `git push -u origin <branch>`: Setzt den Upstream-Branch.

## Zusammenarbeit im Team

- **Branches für jede Person**: Jeder erstellt einen eigenen Branch (z. B. `feature-name`), um unabhängig zu arbeiten.
- **Commit-Nachrichten**: Aussagekräftige Nachrichten wie `fix: behoben Fehler beim Login` oder `feat: neues Layout hinzugefügt`.
- **Regelmäßige Pushes**: Mindestens 1× pro Arbeitssitzung pushen, um Fortschritt transparent zu machen.
- **Merge-Strategie**: Merge nur nach erfolgreichem Pull & Test, um Konflikte zu vermeiden.




