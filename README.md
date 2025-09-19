# 🦅 AdLer Icon Repository

Hochwertige SVG-Icons für deine Projekte. Kostenlos zum Download und sofort einsatzbereit für Web, Mobile und Print.

## 🌐 Live Demo

**➡️ [AdLer Icons Website](https://projektadler.github.io/AdLerIcons/)**

## ✨ Features

- 🎨 **89+ hochwertige SVG-Icons**
- 📱 **Responsive Design** - Mobile & Desktop
- ⚡ **Schnelle Downloads** - Einzeln oder als ZIP
- 🔄 **Icon-Auswahl** - Wähle nur die Icons, die du brauchst
- 🆓 **MIT-Lizenz** - Frei verwendbar für alle Projekte

## 🚀 Verwendung

1. **Besuche die Website**: [AdLer Icons](https://projektadler.github.io/AdLerIcons/)
2. **Icons durchsuchen**: Alle verfügbaren Icons werden automatisch geladen
3. **Auswählen**: Klicke die Checkboxen der gewünschten Icons an
4. **Herunterladen**:
   - Einzelne Icons über den "SVG herunterladen" Button
   - Mehrere Icons über "Ausgewählte Icons herunterladen"
   - Alle Icons über "Alle Icons als ZIP herunterladen"

## 📁 Projektstruktur

```
AdLerIconRepo/
├── index.html               # Hauptseite
├── styles.css               # Styling
├── icons/                   # SVG-Icon-Dateien
├── website-assets/          # Logo und Assets
├── core-data/               # Daten und Übersetzungen
│   ├── translations.js      # Mehrsprachigkeit
│   └── icon-database.js     # Icon-Metadaten
├── functionality-modules/   # JavaScript-Module
│   ├── svg-handler.js       # SVG-Verarbeitung
│   ├── selection-manager.js # Auswahl-Logik
│   ├── icon-grid.js         # Grid-Darstellung
│   ├── download-manager.js  # Download-Funktionen
│   ├── language-manager.js  # Sprachenwechsel
│   └── app-init.js          # Initialisierung
│   └── sticky-download.js   # Initialisierung
└── tests/                   # Playwright-Tests
    ├── user-interactions.spec.js
    └── performance.spec.js
```

## 🛠️ Technologien

- **Vanilla JavaScript** - Keine Frameworks, maximale Performance
- **CSS Grid** - Responsive Icon-Layout
- **JSZip** - Client-seitige ZIP-Erstellung
- **Playwright** - End-to-End Tests
- **GitHub Pages** - Kostenlose Hosting-Lösung

## 📝 Lizenz

Alle Icons stehen unter der [MIT-Lizenz](https://opensource.org/licenses/MIT) und sind frei verwendbar.

## ➕ Neue Icons hinzufügen

### Schritt-für-Schritt Anleitung

Um ein neues Icon zur AdLer Icons Website hinzuzufügen, folge diesen Schritten:

#### 1. **Icon-Datei vorbereiten**

```bash
# Dein SVG-Icon sollte folgende Eigenschaften haben:
- Format: SVG
- Optimiert für Web (kleine Dateigröße)
- Einheitlicher Stil zu bestehenden Icons
- Aussagekräftiger Dateiname (z.B. "new-feature.svg")
```

#### 2. **Icon in den Ordner kopieren**

```bash
# Kopiere deine SVG-Datei in den icons/ Ordner
cp dein-icon.svg icons/
```

#### 3. **Icon-Datenbank aktualisieren**

Öffne die Datei `core-data/icon-database.js` und füge einen neuen Eintrag hinzu:

```javascript
{
    id: 'dein-icon-id',                    // Eindeutige ID (ohne .svg)
    filename: 'dein-icon.svg',             // Exakter Dateiname
    translations: {
        de: {
            title: 'Deutscher Titel',
            desc: 'Deutsche Beschreibung des Icons'
        },
        en: {
            title: 'English Title',
            desc: 'English description of the icon'
        }
    }
}
```

**Wichtige Hinweise:**

- Füge den Eintrag **alphabetisch sortiert** in das Array ein
- Die `id` muss eindeutig und aussagekräftig sein
- Die `filename` muss exakt mit der Datei im `icons/` Ordner übereinstimmen
- Stelle sowohl deutsche als auch englische Übersetzungen bereit

#### 4. **Änderungen testen**

```bash
# Lokalen Server starten
npx http-server . -p 3000

# Website im Browser öffnen: http://localhost:3000
# Überprüfen:
# ✅ Icon wird im Grid angezeigt
# ✅ Titel und Beschreibung sind korrekt
# ✅ Icon kann ausgewählt und heruntergeladen werden
# ✅ Sprachenwechsel funktioniert
```

#### 5. **Tests ausführen**

```bash
# Automatisierte Tests ausführen
npm run test

# Bei Fehlern: Tests mit UI debuggen
npm run test:ui
```

#### 6. **Änderungen committen**

```bash
git add icons/dein-icon.svg core-data/icon-database.js
git commit -m "Add new icon: Dein Icon Name"
git push origin main
```

#### 7. **Deployment überprüfen**

Nach dem Push wird die Website automatisch über GitHub Pages aktualisiert. Überprüfe nach wenigen Minuten:

- [AdLer Icons Website](https://projektadler.github.io/AdLerIcons/)
- Dein neues Icon sollte verfügbar sein

### 🔍 Troubleshooting

**Icon wird nicht angezeigt?**

- ✅ Prüfe den Dateinamen in `icon-database.js`
- ✅ Stelle sicher, dass die SVG-Datei valide ist
- ✅ Überprüfe die Browser-Konsole auf Fehler

**Falsche Beschreibung/Titel?**

- ✅ Überprüfe die Übersetzungen in `icon-database.js`
- ✅ Teste beide Sprachen (DE/EN)

**Download funktioniert nicht?**

- ✅ SVG-Datei muss im `icons/` Ordner sein
- ✅ Filename muss exakt übereinstimmen (Groß-/Kleinschreibung beachten)

## 🤝 Beitragen

1. Repository forken
2. Feature Branch erstellen (`git checkout -b feature/AmazingFeature`)
3. Änderungen committen (`git commit -m 'Add some AmazingFeature'`)
4. Branch pushen (`git push origin feature/AmazingFeature`)
5. Pull Request erstellen

## 📊 Tests

```bash
# Dependencies installieren
npm install

# Tests ausführen
npm run test

# Tests mit UI
npm run test:ui
```

## 🔧 Lokale Entwicklung

```bash
# Repository klonen
git clone https://github.com/yourusername/AdLerIconRepo.git
cd AdLerIconRepo

# Lokalen Server starten
npx http-server . -p 3000

# Öffne http://localhost:3000
```

## 📈 Performance

- ⚡ Lädt in unter 2 Sekunden
- 📱 Mobile-optimiert
- 🔄 Lazy Loading für Icons
- 💾 Effiziente ZIP-Komprimierung

---

**Erstellt mit ❤️ für das AdLer-Projekt**
