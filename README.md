# Test
# Test Projekt (Java + GitHub + Eclipse)

## 📌 Beschreibung

Dieses Projekt dient zum Lernen von:

* Git / GitHub (Versionskontrolle)
* Eclipse (Java Entwicklung)
* Teamarbeit (Branches, Commit, Push, Pull)

---

# 🚀 1. Projekt herunterladen (clone)

Öffne Git Bash und führe aus:

```bash
git clone https://github.com/Nzchupa/Test.git
cd Test
```

---

# 🌿 2. Arbeiten mit Branches

Haupt-Branch:

```text
main
```

Neuen Branch erstellen:

```bash
git checkout main
git pull origin main
git checkout -b feature/aufgabe-name
```

Beispiel:

```bash
git checkout -b feature/java-project
```

---

# 💻 3. Code hinzufügen

1. Kopiere dein Java-Projekt in den Ordner `Test`

Struktur:

```text
Test
├── src
│   └── test
│       └── Test.java
├── README.md
└── .gitignore
```

❗ WICHTIG:

NICHT `.git` aus einem anderen Projekt kopieren

Falls vorhanden:

```text
/project/.git löschen
```

---

# 🧠 4. Änderungen speichern (Commit + Push)

```bash
git add .
git commit -m "Beschreibung der Änderungen"
git push origin feature/branch-name
```

Beispiel:

```bash
git add (Ordner name)
git commit -m "Add Test.java"
git push origin feature/java-project
```

---

# 🔄 5. Updates holen (Pull)

```bash
git checkout main
git pull origin main
```

---

# 🧪 6. Projekt in Eclipse öffnen

1. In Eclipse:

```text
File → Import → Git → Existing local repository
```

2. Wähle:

```text
C:\Users\Macbook\git\Test
```

---

# ⚠️ WICHTIG: Eclipse Fehler

Fehler:

```text
This compilation unit is not on the build path
```

### Lösung:

```text
Right click Projekt → Configure → Convert to Java Project
```

oder:

```text
File → New → Java Project → bestehender Ordner auswählen
```

---

# 🔐 7. GitHub Login (sehr wichtig)

❌ Passwort funktioniert NICHT

Du brauchst einen **Personal Access Token**

👉 https://github.com/settings/tokens

Schritte:

1. Generate new token (classic)
2. Rechte auswählen:

```text
repo
```

3. Token kopieren

In Eclipse eingeben:

```text
User: Nzchupa
Password: TOKEN (nicht dein Passwort!)
```

---

# ❌ Häufige Fehler

### 1. Falscher Befehl

❌ falsch:

```bash
add .
push origin main
```

✔ richtig:

```bash
git add .
git push origin main
```

---

### 2. Datei nicht gefunden

```text
did not match any files
```

👉 Datei existiert nicht im aktuellen Ordner

✔ Lösung:

```bash
ls
```

---

### 3. Falscher Ordner

```text
is outside repository
```

👉 du bist im falschen Projekt

✔ Lösung:

```bash
cd Test
```

---

### 4. Unsichtbare Zeichen im Terminal

```text
command not found: $'\302...'
```

👉 falsches Kopieren

✔ Lösung:

Befehl manuell eingeben

---

### 5. GitHub Push Fehler

```text
git-receive-pack not permitted
```

👉 kein Zugriff

✔ Lösung:

Token verwenden (siehe oben)

---

### 6. Verschachteltes Git-Projekt

```text
embedded git repository
```

👉 du hast ein Projekt mit eigenem `.git` eingefügt

✔ Lösung:

```bash
rm -rf projekt/.git
```

---

# ✔️ Regeln für Teamarbeit

* Niemals direkt in `main` arbeiten
* Jede Aufgabe = eigener Branch
* Immer `git pull` vor der Arbeit
* Nach der Arbeit → Pull Request erstellen
* Code immer beschreiben (Commit Message)

---

# ✔️ Kurz-Zusammenfassung

```bash
git clone URL
cd Test
git checkout -b feature/name
git add .
git commit -m "..."
git push origin feature/name
```

---

# 📌 Ziel

Alle Teammitglieder können:

* Projekt klonen
* Code hinzufügen
* Änderungen pushen
* Gemeinsam arbeiten ohne Fehler

# 🔄 Neue Version des Codes herunterladen (über Eclipse)

Bevor du mit der Arbeit beginnst, musst du immer die neueste Version vom Projekt holen.

## Schritt 1: Zum main-Branch wechseln

1. Rechtsklick auf das Projekt
2. Wähle:

```text
Team → Switch To → main
```

---

## Schritt 2: Änderungen herunterladen (Pull)

1. Rechtsklick auf das Projekt
2. Wähle:

```text
Team → Pull
```

👉 Eclipse lädt die neuesten Änderungen von GitHub herunter

---

## Schritt 3: Neuen Branch erstellen

1. Rechtsklick auf das Projekt
2. Wähle:

```text
Team → Switch To → New Branch
```

3. Name eingeben:

```text
feature/aufgabe-name
```

Beispiel:

```text
feature/login
```

4. Bestätigen

---

## Wichtige Regel

Vor jeder neuen Aufgabe immer:

```text
1. main auswählen
2. Pull machen
3. neuen Branch erstellen
```

---

## Typischer Fehler

❌ Kein Pull gemacht:

```text
→ alter Code
→ Konflikte beim Push
→ Probleme im Team
```

✔ Lösung:

```text
Immer zuerst Pull
```

---

## Kurz-Zusammenfassung

```text
Team → Switch To → main
Team → Pull
Team → Switch To → New Branch
```

---

# ✔️ Ziel

Alle Teammitglieder arbeiten immer:

* mit der neuesten Version
* ohne Konflikte
* sauber getrennt in eigenen Branches

* # 💾 Änderungen speichern (Commit) über Eclipse

Commit bedeutet: Änderungen lokal speichern.

## Schritt 1: Änderungen auswählen

1. Rechtsklick auf das Projekt
2. Wähle:

```text
Team → Commit
```

---

## Schritt 2: Dateien auswählen

Im Fenster:

```text
Unstaged Changes → markieren → nach Staged Changes verschieben
```

---

## Schritt 3: Commit Message schreiben

Beispiel:

```text
Add Test.java
Fix login error
Update UI
```

---

## Schritt 4: Commit ausführen

```text
Commit
```

👉 speichert Änderungen lokal

---

## Schritt 5: Änderungen auf GitHub hochladen (Push)

```text
Commit and Push
```

oder:

```text
Team → Push
```

---

# 🔄 WICHTIG: Commit ≠ Update

❌ Falsch denken:

```text
Commit lädt neue Version herunter
```

✔ Richtig:

```text
Commit → speichert deine Änderungen
Pull → lädt neue Version vom Server
Push → lädt deine Änderungen hoch
```

---

# ✔️ Richtiger Ablauf in Eclipse

Vor der Arbeit:

```text
Team → Switch To → main
Team → Pull
Team → Switch To → New Branch
```

Nach der Arbeit:

```text
Team → Commit
Team → Push
```

---

# ❗ Typische Fehler

### 1. Nur Commit gemacht

```text
→ Änderungen sind NICHT auf GitHub
```

✔ Lösung:

```text
Immer auch Push machen
```

---

### 2. Kein Pull gemacht

```text
→ alter Code
→ Konflikte möglich
```

✔ Lösung:

```text
Vorher immer Pull
```

---

# ✔️ Kurz-Zusammenfassung

```text
Commit → lokal speichern
Push → auf GitHub senden
Pull → neue Version holen
```

