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
git init                   # Neues lokales Git-Repository erstellen
git status                 # Zeigt den aktuellen Status der Arbeitsverzeichnisse
git add .                  # Stellt alle Dateien zur Aufnahme bereit
git commit -m "Nachricht"  # Änderungen speichern mit Kommentar
git log                    # Zeigt den Verlauf der Commits an
git merge <branch>         # Merge eines Branches in den aktuellen
git merge --abort          # Merge-Konflikt abbrechen
git rebase <branch>        # Spielt die eigenen Commits auf den neuesten Stand von branch ab.
   ➤ Vorteil: Saubere lineare Historie.
   ⚠️ Achtung: Nur bei lokalen Branches verwenden, die noch nicht gepusht wurden.
git cherry-pick <commit>   # Übernimmt einen bestimmten Commit aus einem anderen Branch.
   ➤ Nützlich, um gezielt Änderungen zu übertragen.
   ⚠️ Mögliche Konflikte, wenn sich der Kontext geändert hat.
git reset --hard <commit>  # Setzt den aktuellen Branch auf einen bestimmten Commit zurück und verwirft Änderungen.
  - ➤ Kann zum "Zurückspringen" verwendet werden.
  - ⚠️ Achtung: Verwirft Änderungen endgültig, wenn sie nicht gespeichert wurden.
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


## Markdown erlaubt einfache Formatierung:

- `#` bis `###` = Titel
- `*kursiv*` oder `**fett**`
- Listen mit `-` oder `*`
- Codeblöcke mit ```bash
- Tabellen mit dem [Generator](https://www.tablesgenerator.com/markdown_tables)


# Bewertung des Repositories: gitstarted-zusammenfassung-ali-akgoz-runsheng-song-und-tom

## 1. Fachbegriffe
- **Erreichte Punkte:** 2
- **Begründung:** Die Fachbegriffe wie *Repository*, *Branch*, *Commit*, *Merge-Konflikt* usw. sind korrekt verwendet und größtenteils vollständig. 
Es fehlen die Begriffe "Working Directory" und "Staging Area", die unverzichtbar sind in diesem Kontext!


## 2. Befehle – lokale Arbeit
- **Erreichte Punkte:** 2
- **Begründung:** Die Befehle zur lokalen Arbeit mit Git (z. B. `git init`, `git add`, `git commit`, `git merge`) sind korrekt und vollständig aufgeführt. 
Die Formatierung ist übersichtlich, und es gibt Hinweise auf z.B. Merge-Konflikte. 
Die Markdown-Struktur ist gut lesbar.
Die Erläuterungen sind teilweise sehr knapp.
Es fehlen z.B. auch die Zusätze bei `git reset` (soft, mixed)
Weitere Hinweise auf häufige Fehlermeldungen und den Umgang damit wären wünschenswert (z.B. git commit ohne vohriges git add oder Fehlermeldung "nothing to commit, Working tree clean")

## 3. Befehle – entfernte Arbeit
- **Erreichte Punkte:** 3
- **Begründung:** Die wichtigsten Befehle zur Arbeit mit Remote-Repositories (z. B. `git clone`, `git push`, `git pull`, `git remote`) sind vorhanden und korrekt. 
Es fehlen jedoch teilweise Hinweise auf typische Stolperfallen (z.B. häufig auftretende Fehlermeldungen und den Umgang damit).
Die Lesbarkeit ist gut, aber etwas mehr Tiefe wäre wünschenswert.

## 4. Güte der Zusammenarbeit
- **Erreichte Punkte:** 2
- **Begründung:** Es gibt mehrere Commits, die regelmäßig erfolgt sind. 
Die Commit-Nachrichten sind größtenteils nachvollziehbar, aber nicht immer sehr aussagekräftig. 
Es wurde mit Branches gearbeitet, allerdings enthält der Haupt-Branch auch andere Commits als nur Merges. 
Für die volle Punktzahl wäre eine konsequentere Branch-Nutzung und klarere Commit-Struktur nötig.

## Gesamtbewertung:
| Kriterium               | Punkte |
|------------------------|--------|
| Fachbegriffe           | 2      |
| Lokale Arbeit          | 2      |
| Entfernte Arbeit       | 3      |
| Zusammenarbeit         | 2      |
| **Gesamt**             | **9/12** |

--> **75% --> gut(11 NP.)**

---

## Verbesserungsvorschläge

### 1. Fachbegriffe
- Fügt Beispiele oder kleine Szenarien hinzu, z. B.:
  - „Wenn du eine Datei geändert hast, musst du sie mit `git add` zur Staging-Area hinzufügen, bevor du sie mit `git commit` speicherst.“
  - "Es kann sein, dass du folgende Fehlermeldung erhältst:  "nothing to commit, Working tree clean"; in diesem Fall ..."

### 2. Lokale Arbeit
- Ihr könntet noch typische Fehler erwähnen, z. B.:
  - „Wenn du `git commit` ohne `-m` benutzt, öffnet sich ein Editor, z.B. der VIM – das kann verwirrend sein. Du kannst aus dem VIM herauskommen, in dem ...“
- Vielleicht ein Mini-Tutorial oder eine Schritt-für-Schritt-Anleitung einbauen.

### 3. Entfernte Arbeit
- Ergänzt Hinweise wie:
  - „Wenn du zum ersten Mal auf ein Remote-Repo pushst, musst du `--set-upstream` verwenden.“
  - „Typischer Fehler: `git push` schlägt fehl, wenn du keine Schreibrechte hast.“
