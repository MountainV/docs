# Git-Workflow

So bringen wir Änderungen bei MountainV ins `main`.

## Überblick

```
Issue  →  Branch  →  Commits  →  Pull Request  →  Review  →  Merge
```

Kein direkter Push auf `main`. Jede Änderung läuft über einen Pull Request.

## 1. Branch anlegen

Nach dem [Namensschema](../standards/namenskonventionen.md):

```bash
git checkout main
git pull
git checkout -b docs/mein-thema
```

## 2. Arbeiten & committen

- Ein Thema pro Branch.
- Commit-Nachrichten im Imperativ, auf Deutsch.

```bash
git add -A
git commit -m "Git-Workflow-Guide ergaenzen"
```

## 3. Pull Request öffnen

```bash
git push -u origin docs/mein-thema
```

Dann auf GitHub den PR öffnen. Dabei:

- Die PR-Vorlage ausfüllen.
- Das zugehörige Issue verlinken: `Closes #123`.
- Passende Labels setzen (`type: ...`, ggf. `status: review`).

## 4. Review & Merge

- Mindestens **eine Freigabe** nötig.
- Feedback einarbeiten, bis das Review grün ist.
- Merge per **Squash**, damit `main` eine saubere Historie behält.
- Branch nach dem Merge löschen.

## Spickzettel

| Schritt | Befehl |
|--------|--------|
| Aktuellen Stand holen | `git pull` |
| Branch wechseln | `git checkout -b <name>` |
| Änderungen ansehen | `git status` / `git diff` |
| Hochladen | `git push -u origin <name>` |
