# Beitragen zur Schnitzler Family App

Vielen Dank für dein Interesse, zur Schnitzler Family App beizutragen! 🎉

## 🚀 Wie kann ich beitragen?

### Bugs melden

Wenn du einen Bug findest:

1. Prüfe ob der Bug bereits gemeldet wurde ([Issues](../../issues))
2. Falls nicht, erstelle ein neues Issue mit:
   - Aussagekräftiger Titel
   - Beschreibung des Problems
   - Schritte zur Reproduktion
   - Browser & Version
   - Screenshots (falls relevant)

### Feature-Vorschläge

Hast du eine Idee für ein neues Feature?

1. Prüfe ob die Idee bereits vorgeschlagen wurde
2. Erstelle ein neues Issue mit Tag `enhancement`
3. Beschreibe:
   - Was soll das Feature tun?
   - Warum ist es nützlich?
   - Wie könnte es umgesetzt werden?

### Code beitragen

1. **Fork das Repository**
   ```bash
   git clone https://github.com/dein-username/schnitzler-family-app.git
   cd schnitzler-family-app
   ```

2. **Erstelle einen Feature Branch**
   ```bash
   git checkout -b feature/mein-neues-feature
   ```

3. **Mache deine Änderungen**
   - Halte dich an den bestehenden Code-Stil
   - Teste deine Änderungen gründlich
   - Kommentiere komplexen Code

4. **Commit deine Änderungen**
   ```bash
   git add .
   git commit -m "Add: Beschreibung der Änderung"
   ```

   Commit-Präfixe:
   - `Add:` - Neues Feature
   - `Fix:` - Bug-Fix
   - `Update:` - Verbesserung
   - `Remove:` - Entfernung
   - `Docs:` - Dokumentation

5. **Push zum Branch**
   ```bash
   git push origin feature/mein-neues-feature
   ```

6. **Erstelle einen Pull Request**

## 📝 Code-Richtlinien

### JavaScript

- ES6+ Syntax verwenden
- Keine externen Dependencies
- Klare, beschreibende Variablennamen
- Kommentare für komplexe Logik

```javascript
// ✅ Gut
function calculateDailyEarnings(monthlyAllowance, tasksCompleted, totalTasks) {
    const dailyBase = monthlyAllowance / 30;
    const completionRate = tasksCompleted / totalTasks;
    return dailyBase * completionRate;
}

// ❌ Nicht gut
function calc(m,t,tt) {
    return (m/30)*(t/tt);
}
```

### CSS

- CSS-Variablen verwenden (`:root`)
- Mobile-First-Ansatz
- Klare Klassennamen

```css
/* ✅ Gut */
.task-item {
    padding: 16px;
    border-radius: var(--radius-sm);
}

/* ❌ Nicht gut */
.ti {
    padding: 16px;
    border-radius: 8px;
}
```

### HTML

- Semantische HTML5-Tags
- Accessibility beachten (aria-labels, alt-Texte)
- Responsive Bilder

## 🧪 Testing

Teste deine Änderungen in:
- Chrome (aktuell)
- Firefox (aktuell)
- Safari (aktuell)
- Mobile Browser (iOS/Android)

Testszenarien:
- [ ] Login funktioniert
- [ ] Aufgaben können abgehakt werden
- [ ] Taschengeld wird korrekt berechnet
- [ ] Backup/Import funktioniert
- [ ] Dark Mode funktioniert
- [ ] Mobile-Ansicht ist verwendbar

## 📚 Dokumentation

Wenn du Code änderst:
- Aktualisiere die README wenn nötig
- Füge Code-Kommentare hinzu
- Update das Changelog

## 🎨 Design-Prinzipien

1. **Einfachheit**: Die App soll einfach zu bedienen sein
2. **Familienfreundlich**: Für Kinder und Eltern gleichermaßen
3. **Keine Abhängigkeiten**: Pure HTML/CSS/JS
4. **Offline-First**: Funktioniert ohne Internet
5. **Privacy**: Keine Daten-Übertragung an Server

## 🚫 Was wird nicht akzeptiert

- Code mit externen Dependencies (außer CDN für Icons)
- Features die Server/Backend benötigen
- Tracking oder Analytics
- Nicht-familienfreundlicher Content
- Code der gegen die MIT-Lizenz verstößt

## 💬 Fragen?

- Öffne eine [Discussion](../../discussions)
- Oder erstelle ein Issue mit dem Tag `question`

## 🙏 Vielen Dank!

Jeder Beitrag hilft, die App besser zu machen! ❤️
