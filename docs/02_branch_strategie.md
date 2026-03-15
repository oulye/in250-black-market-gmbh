# Git Branch Strategie 

Um Chaos, Überschreibungen und unkontrollierte Releases zu verhindern,
verwendet die Black Market Software GmbH die folgende strukturierte Branching-Strategie:

---

## 1. Hauptbranch "main"

- Enthält immer den stabilen, produktionsreifen Code
- Nur PR dürfen in "main" gemerged werden
- direktes Pushen ist nicht erlaubt (Branch Protection)

---

## 2. Feature Branches

- Name = feat/<beschreibung>
- werden immer aus "main" erstellt
- Dienen der Entwicklung neuer Funktionen
- Nach Fertigstellung: PR -> Code Review -> Merge

---

## 3. Bugfix Branches
- Name = fix/<beschreibung>
- Dienen der behebung kleiner Fehler
- werden immer aus "main" erstellt
- Nach Behebung: PR -> Merge

---

## 4. Hotfix Branches
- Name = hotfix/<beschreibung>
- Für kritische Fehler, die sofort behoben werden müssen
1. aus "main" erstellen
2. Fehler beheben
3. Direkte Merge nach "main"

---

## 5. Release Tags

- Jeder stabile Stand auf "main" erhält einen Tag
- Beipiel: "v1.0", "v1.1", "v2.0"
- Tags ermöglichen Rollbacks und nachvollziehbare Versionierung

---

## 🔁 6. Pull Request Workflow

1. Entwickler erstellt Feature- oder Fix-Branch  
2. Arbeitet lokal  
3. Commit → Push  
4. Pull Request erstellen  
5. Team prüft Code  
6. Merge nur über PR nach "main"

---

## 🛡️ 7. Schutz des main‑Branches

- Direkte Pushes sind deaktiviert
- PRs benötigen mindestens 1 Review
- CI muss bestehen

---

