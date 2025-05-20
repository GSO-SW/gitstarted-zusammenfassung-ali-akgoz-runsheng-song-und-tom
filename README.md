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

