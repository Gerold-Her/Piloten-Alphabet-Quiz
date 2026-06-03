# Piloten-Alphabet Quiz ✈️

Ein interaktives Quiz zum Lernen und Üben des ICAO-Alphabets (NATO-Phonetik), direkt im Browser – ohne Installation, ohne App.

## Demo

👉 [https://gerold-her.github.io/Piloten-Alphabet-Quiz](https://gerold-her.github.io/Piloten-Alphabet-Quiz)

---

## Features

- **20 zufällige Fragen** pro Durchgang – kein Buchstabe folgt direkt auf sich selbst
- **Sofortiges Feedback** – richtige und falsche Antwort farblich hervorgehoben
- **Referenztabelle** – alle 26 Buchstaben jederzeit ausklappbar
- **Top 10 Bestenliste** – gespeichert in Firebase Firestore, live nach dem Quiz
- **Dark Mode** – automatisch je nach Systemeinstellung
- **Mobile-optimiert** – stabile Darstellung auch wenn die Tastatur aufgeht
- **Kein Framework** – reines HTML, CSS und JavaScript in einer einzigen Datei

---

## Das ICAO-Alphabet

| Buchstabe | Wort | Buchstabe | Wort |
|-----------|------|-----------|------|
| A | Alpha | N | November |
| B | Bravo | O | Oscar |
| C | Charlie | P | Papa |
| D | Delta | Q | Quebec |
| E | Echo | R | Romeo |
| F | Foxtrot | S | Sierra |
| G | Golf | T | Tango |
| H | Hotel | U | Uniform |
| I | India | V | Victor |
| J | Juliett | W | Whiskey |
| K | Kilo | X | X-ray |
| L | Lima | Y | Yankee |
| M | Mike | Z | Zulu |

---

## Technik

| Bereich | Technologie |
|---------|-------------|
| Frontend | HTML, CSS, JavaScript (vanilla) |
| Datenbank | Firebase Firestore |
| Sicherheit | Firebase App Check + reCAPTCHA v3 |
| Hosting | GitHub Pages |

### Firebase Sicherheitsregeln

Die Firestore-Datenbank ist mit folgenden Regeln abgesichert:

- Bestenliste ist öffentlich **lesbar**
- Einträge können **nur erstellt**, nicht geändert oder gelöscht werden
- Pflichtfelder (`name`, `cor`, `timestamp`) und Wertebereich (0–20 Punkte, Name max. 50 Zeichen) werden serverseitig geprüft
- Alle anderen Collections sind vollständig gesperrt
- Firebase App Check mit reCAPTCHA v3 verhindert direkten API-Zugriff ohne Browser-Kontext

---

## Lokale Nutzung

Die App benötigt keinen Server oder Build-Schritt:

```bash
git clone https://github.com/Gerold-Her/Piloten-Alphabet-Quiz.git
cd Piloten-Alphabet-Quiz
# index.html direkt im Browser öffnen
```

---

## Impressum

Gerold Herbsthofer, Linz 2026
