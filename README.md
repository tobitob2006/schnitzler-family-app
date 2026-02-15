# 👨‍👩‍👧‍👦 Schnitzler Family App

Eine moderne, benutzerfreundliche Familien-App zur Verwaltung von Aufgaben, Taschengeld und Familienorganisation.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ Features

- 📋 **Aufgabenverwaltung** - Tägliche Aufgaben für Kinder
- 💰 **Taschengeld-Tracker** - Automatische Berechnung basierend auf erledigten Aufgaben
- 👨‍👩‍👧‍👦 **Multi-User** - Separate Profile für bis zu 4 Kinder + Eltern
- 💬 **Nachrichten** - Kommunikation zwischen Kindern und Eltern
- 🎨 **Anpassbar** - Farbschemas, Avatars, Dark Mode
- 📱 **Responsive** - Funktioniert auf Desktop, Tablet und Smartphone
- ☁️ **Einfache Synchronisation** - Datei-basierte Sync über Cloud-Dienste
- 🔒 **Sicher** - PIN-geschützte Admin-Bereiche

## 🚀 Live Demo

[**Hier klicken für Live-Demo**](https://dein-github-username.github.io/schnitzler-family-app/)

## 📦 Installation

### Option 1: GitHub Pages (Empfohlen)

1. **Repository forken**
   ```
   Klicke auf "Fork" oben rechts
   ```

2. **GitHub Pages aktivieren**
   ```
   Settings → Pages → Source: main branch → Save
   ```

3. **Fertig!**
   ```
   Deine App ist erreichbar unter:
   https://dein-username.github.io/schnitzler-family-app/
   ```

### Option 2: Lokal nutzen

1. **Repository klonen**
   ```bash
   git clone https://github.com/dein-username/schnitzler-family-app.git
   cd schnitzler-family-app
   ```

2. **Öffnen**
   ```bash
   # Einfach index.html im Browser öffnen
   open index.html
   # oder
   python -m http.server 8000
   ```

### Option 3: Download

1. [ZIP herunterladen](../../archive/refs/heads/main.zip)
2. Entpacken
3. `index.html` im Browser öffnen

## 🎯 Schnellstart

### Erste Schritte

1. **App öffnen**
   - Öffne `index.html` in deinem Browser

2. **Admin-Zugang**
   - Klicke auf "Admin-Einstellungen"
   - Standard-PIN: `1234` (bitte ändern!)

3. **Kinder einrichten**
   - Namen, Alter und Taschengeld eingeben
   - Speichern

4. **Loslegen!**
   - Kinder können sich anmelden und Aufgaben erledigen

## 📖 Benutzerhandbuch

### Für Eltern

#### Konfiguration
1. Admin → "Admin-Einstellungen" → PIN: `1234`
2. Kinder einrichten (Name, Alter, Taschengeld)
3. Optional: Avatar-Bilder hochladen

#### Synchronisation
1. Admin → "Backup herunterladen"
2. Datei in Google Drive/Dropbox speichern
3. Auf anderen Geräten: Datei hochladen

#### Nachrichten lesen
1. Als Eltern anmelden
2. Nachrichten von Kindern werden angezeigt

### Für Kinder

#### Aufgaben erledigen
1. Anmelden mit deinem Namen
2. Tab "Aufgaben"
3. Aufgaben antippen zum Abhaken
4. "Tag abschließen" wenn fertig

#### Taschengeld sehen
1. Tab "Guthaben"
2. Aktueller Kontostand und Prognose

#### Nachricht senden
1. Tab "Nachricht"
2. Text eingeben und senden

## 🔧 Konfiguration

### Admin-PIN ändern

```javascript
// Standard: 1234
// Ändern in der App: Admin → "Admin-PIN ändern"
```

### Taschengeld-Berechnung

```javascript
// Formel:
Verdienst pro Tag = (Monatliches Taschengeld / 30) * (Erledigte Aufgaben / Gesamt Aufgaben)

// Beispiel:
// 30€ pro Monat, 4 von 5 Aufgaben erledigt:
// (30 / 30) * (4 / 5) = 0,80€ pro Tag
```

### Anpassungen

Die App speichert alle Daten im Browser LocalStorage:

```javascript
// Daten ansehen (Browser Console):
localStorage.getItem('familyData')

// Alle Daten löschen:
localStorage.clear()
```

## 📱 Cloud-Synchronisation

Die App nutzt ein einfaches, datei-basiertes Sync-System:

### Workflow

1. **Backup erstellen**
   ```
   Admin → "Backup herunterladen"
   → Datei: schnitzler-backup-YYYY-MM-DD.json
   ```

2. **In Cloud speichern**
   - Google Drive
   - Dropbox
   - iCloud
   - OneDrive

3. **Auf anderen Geräten laden**
   ```
   Admin → Backup hochladen → Datei auswählen
   ```

### Vorteile

✅ Funktioniert überall - keine API-Blockierung
✅ Vollständige Kontrolle über deine Daten
✅ Funktioniert offline
✅ Kein Account nötig

## 🎨 Anpassung

### Farben ändern

```javascript
// In index.html, CSS-Variablen:
:root {
    --primary: #4f46e5;    // Hauptfarbe
    --accent: #f59e0b;     // Akzentfarbe
    --success: #10b981;    // Erfolgsfarbe
}
```

### Aufgaben-Pool anpassen

```javascript
// In app.generateTasks():
const pool = [
    "Zimmer aufräumen",
    "Bett machen",
    "Hausaufgaben",
    // Eigene Aufgaben hinzufügen...
];
```

## 🔒 Sicherheit & Datenschutz

### Datenspeicherung

- **Lokal**: Alle Daten werden im Browser gespeichert (localStorage)
- **Keine Server**: Keine Daten werden an externe Server gesendet
- **Privat**: Nur du hast Zugriff auf deine Daten

### Backups

- Backups sind unverschlüsselte JSON-Dateien
- Speichere Backups sicher
- Teile Backups nur mit Familienmitgliedern

### Empfehlungen

1. ✅ Admin-PIN ändern (nicht "1234" verwenden)
2. ✅ Regelmäßige Backups erstellen
3. ✅ Backups sicher speichern
4. ✅ Bei öffentlicher Nutzung: Browser-Daten löschen

## 🛠️ Entwicklung

### Technologie-Stack

- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Storage**: Browser LocalStorage
- **Keine Dependencies**: Keine externen Bibliotheken
- **Progressive Web App**: Kann als App installiert werden

### Struktur

```
schnitzler-family-app/
├── index.html          # Haupt-App
├── README.md           # Diese Datei
├── LICENSE             # MIT Lizenz
└── docs/               # Dokumentation
    ├── screenshots/    # Screenshots
    └── ANLEITUNG.md    # Deutsche Anleitung
```

### Beitragen

Contributions sind willkommen!

1. Fork das Repository
2. Erstelle einen Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit deine Änderungen (`git commit -m 'Add AmazingFeature'`)
4. Push zum Branch (`git push origin feature/AmazingFeature`)
5. Öffne einen Pull Request

## 📝 Changelog

### Version 1.0.0 (2025-02-15)

- ✨ Initiales Release
- 📋 Aufgabenverwaltung
- 💰 Taschengeld-Tracker
- 👨‍👩‍👧‍👦 Multi-User Support
- 💬 Nachrichten-System
- ☁️ Datei-basierte Synchronisation
- 🎨 Dark Mode
- 📱 Responsive Design

## 🐛 Bekannte Probleme

- Bilder sollten unter 500KB sein (sonst Performance-Probleme)
- LocalStorage ist auf ~5-10MB begrenzt

## 📞 Support

- **Issues**: [GitHub Issues](../../issues)
- **Diskussionen**: [GitHub Discussions](../../discussions)
- **Wiki**: [Wiki](../../wiki)

## 📄 Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert - siehe [LICENSE](LICENSE) Datei für Details.

## 🙏 Danksagungen

- Icons von [Flaticon](https://www.flaticon.com/)
- Design-Inspiration von modernen Family-Management-Apps
- Entwickelt mit ❤️ für Familien

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=dein-username/schnitzler-family-app&type=Date)](https://star-history.com/#dein-username/schnitzler-family-app&Date)

---

**Made with ❤️ for families | [Report Bug](../../issues) | [Request Feature](../../issues)**
