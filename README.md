# Versicherungsmakler Verzeichnis

**Die führenden Versicherungsmakler vergleichen**

Eine umfassende Verzeichniswebsite zur Verwaltung und Präsentation von Versicherungsmakler-Einträgen mit modernem, responsivem Design.

---

## Inhaltsverzeichnis

- [Überblick](#überblick)
- [Funktionen](#funktionen)
- [Dateistruktur](#dateistruktur)
- [Setup und Deployment](#setup-und-deployment)
- [Custom Domain Einrichtung](#custom-domain-einrichtung)
- [Anpassungsanleitungen](#anpassungsanleitungen)
- [Verzeichniseinträge verwalten](#verzeichniseinträge-verwalten)
- [Styling und Design](#styling-und-design)
- [Fehlerbehebung](#fehlerbehebung)
- [Ressourcen und Support](#ressourcen-und-support)

---

## Überblick

Das Versicherungsmakler Verzeichnis ist eine moderne Verzeichniswebsite, die Versicherungsmakler in einem übersichtlichen 3-Spalten-Gitter-Layout präsentiert. Die Website ist vollständig responsiv, suchmaschinenoptimiert und einfach zu verwalten.

### Hauptmerkmale:
- **Responsive Design**: Optimiert für Desktop, Tablet und Mobilgeräte
- **3-Spalten Grid Layout**: Professionelle Präsentation von Verzeichniseinträgen
- **Hero-Sektion**: Ansprechende Kopfzeile mit Suchfunktion
- **Kategorisierung**: Organisierte Kategorien für bessere Navigation
- **Suchfunktionalität**: Benutzer können Makler schnell finden
- **SEO-optimiert**: Eingebaute Best Practices für Suchmaschinen

---

## Funktionen

### Verzeichnisverwaltung
- Einfaches Hinzufügen und Bearbeiten von Makler-Einträgen
- Kategorisierung nach Versicherungstypen
- Detaillierte Informationen für jeden Eintrag
- Kontaktinformationen und Links

### Benutzeroberfläche
- Intuitive Navigation
- Filterung nach Kategorien
- Suchleiste für schnelle Suche
- Responsive Kartendesign für Einträge

### Technische Features
- HTML5 und CSS3
- Mobile-First Design
- Schnelle Ladezeiten
- Barrierefreies Markup

---

## Dateistruktur

```
versicherungsmakler-verzeichnis/
├── index.html              # Hauptseite
├── css/
│   └── styles.css          # Hauptstylesheet
├── js/
│   └── script.js           # JavaScript-Funktionalität
├── images/
│   ├── logo.png            # Website-Logo
│   ├── hero-bg.jpg         # Hero-Hintergrund
│   └── icons/              # Icon-Assets
├── data/
│   └── makler.json         # Verzeichnisdaten (optional)
├── README.md               # Diese Datei
└── .gitignore              # Git-Ignore-Datei
```

### Dateienbeschreibungen

| Datei | Zweck |
|-------|-------|
| `index.html` | Hauptseite mit HTML-Struktur |
| `css/styles.css` | Alle Styling- und Layout-Regeln |
| `js/script.js` | Interaktivität und Funktionalität |
| `data/makler.json` | Strukturierte Verzeichnisdaten |

---

## Setup und Deployment

### Lokale Installation

1. **Repository klonen oder herunterladen**
   ```bash
   git clone https://github.com/yourusername/versicherungsmakler-verzeichnis.git
   cd versicherungsmakler-verzeichnis
   ```

2. **Lokalen Server starten**
   - Verwenden Sie einen lokalen Server wie Live Server in VS Code
   - Oder nutzen Sie Python: `python -m http.server 8000`
   - Öffnen Sie `http://localhost:8000` im Browser

3. **Dateien anpassen**
   - Bearbeiten Sie HTML-, CSS- und JavaScript-Dateien nach Bedarf
   - Testen Sie Änderungen lokal

### Deployment auf Hosting

#### Option 1: GitHub Pages (Kostenlos)
1. Push Sie Ihr Repository zu GitHub
2. Gehen Sie zu Repository-Einstellungen
3. Aktivieren Sie "GitHub Pages" unter "Pages"
4. Wählen Sie den `main`-Branch als Quelle
5. Ihre Website ist unter `https://yourusername.github.io/repo-name` verfügbar

#### Option 2: Netlify (Kostenlos mit Optionen)
1. Verbinden Sie Ihr GitHub-Repository mit Netlify
2. Netlify baut und deployed automatisch
3. Erhalten Sie eine kostenlose `netlify.app`-Domain
4. Verbinden Sie eine Custom Domain in den Einstellungen

#### Option 3: Traditionelles Hosting
1. Laden Sie alle Dateien auf Ihren FTP-Server hoch
2. Stellen Sie sicher, dass `index.html` im Root-Verzeichnis liegt
3. Testen Sie die Website im Browser

### Deployment-Checkliste
- [ ] Alle Links sind korrekt
- [ ] Bilder werden geladen
- [ ] Suchfunktion funktioniert
- [ ] Mobile-Ansicht sieht gut aus
- [ ] Alle Verzeichniseinträge sind sichtbar
- [ ] Kontaktinformationen sind aktuell
- [ ] Meta-Tags sind ausgefüllt

---

## Custom Domain Einrichtung

### Domain registrieren
1. Registrieren Sie eine Domain bei einem Domain-Registrar:
   - GoDaddy
   - Namecheap
   - 1&1
   - Strato

### Domain mit Hosting verbinden

#### Für GitHub Pages:
1. Gehen Sie zu Ihrem GitHub-Repository
2. Navigieren Sie zu Settings → Pages
3. Unter "Custom domain" geben Sie Ihre Domain ein
4. Klicken Sie "Save"
5. GitHub erstellt automatisch CNAME-Datei
6. Aktualisieren Sie DNS-Einstellungen bei Ihrem Registrar:
   - Setzen Sie A-Records auf GitHub's IP-Adressen
   - Oder erstellen Sie einen CNAME-Record

#### Für Netlify:
1. Gehen Sie zu Ihre Site → Settings → Domain Management
2. Klicken Sie "Add domain"
3. Geben Sie Ihre Domain ein
4. Aktualisieren Sie Nameserver bei Ihrem Registrar
5. Oder konfigurieren Sie DNS-Records

#### Für traditionelles Hosting:
1. Melden Sie sich im Hosting-Control-Panel an
2. Gehen Sie zu Domain/DNS-Einstellungen
3. Setzen Sie Nameserver auf die des Hosters
4. Oder konfigurieren Sie A-Records direkt

### SSL-Zertifikat
- GitHub Pages und Netlify bieten kostenlose HTTPS
- Für traditionelles Hosting: Let's Encrypt (kostenlos) verwenden
- Stellen Sie sicher, dass HTTPS aktiviert ist

---

## Anpassungsanleitungen

### Hero-Sektion anpassen

Die Hero-Sektion ist der erste Eindruck Ihrer Website. So passen Sie sie an:

#### Hintergrund ändern
Bearbeiten Sie `css/styles.css`:
```css
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    background-image: url('images/hero-bg.jpg');
    background-size: cover;
    background-position: center;
    height: 400px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
}
```

#### Titel und Beschreibung ändern
Bearbeiten Sie `index.html`:
```html
<section class="hero">
    <div class="hero-content">
        <h1>Versicherungsmakler Verzeichnis</h1>
        <p>Die führenden Versicherungsmakler vergleichen</p>
        <input type="text" id="searchBox" placeholder="Nach Makler suchen...">
    </div>
</section>
```

#### Suchfunktion anpassen
Bearbeiten Sie `js/script.js`:
```javascript
document.getElementById('searchBox').addEventListener('keyup', function(e) {
    const searchTerm = e.target.value.toLowerCase();
    const entries = document.querySelectorAll('.entry-card');
    
    entries.forEach(entry => {
        const text = entry.textContent.toLowerCase();
        entry.style.display = text.includes(searchTerm) ? 'block' : 'none';
    });
});
```

---

## Verzeichniseinträge verwalten

### Neue Einträge hinzufügen

#### Methode 1: Direkt in HTML

Öffnen Sie `index.html` und fügen Sie einen neuen Eintrag in das Grid hinzu:

```html
<div class="entries-grid">
    <div class="entry-card" data-category="makler">
        <div class="entry-image">
            <img src="images/makler1.jpg" alt="Makler Name">
        </div>
        <div class="entry-content">
            <h3>Makler Name</h3>
            <p class="category">Kategorie: Versicherungsmakler</p>
            <p class="description">Kurze Beschreibung des Maklers und Spezialgebiete.</p>
            <div class="entry-details">
                <p><strong>Telefon:</strong> +49 (0) 123 456789</p>
                <p><strong>Email:</strong> info@makler.de</p>
                <p><strong>Website:</strong> <a href="https://www.makler.de" target="_blank">www.makler.de</a></p>
            </div>
            <div class="entry-footer">
                <span class="rating">★★★★★ (4.8)</span>
            </div>
        </div>
    </div>
</div>
```

#### Methode 2: Mit JSON-Datei (für größere Verzeichnisse)

Erstellen Sie `data/makler.json`:
```json
{
    "makler": [
        {
            "id": 1,
            "name": "Makler Name",
            "category": "Versicherungsmakler",
            "image": "images/makler1.jpg",
            "description": "Kurze Beschreibung des Maklers",
            "phone": "+49 (0) 123 456789",
            "email": "info@makler.de",
            "website": "https://www.makler.de",
            "rating": 4.8
        },
        {
            "id": 2,
            "name": "Zweiter Makler",
            "category": "Versicherungsmakler",
            "image": "images/makler2.jpg",
            "description": "Beschreibung des zweiten Maklers",
            "phone": "+49 (0) 987 654321",
            "email": "kontakt@makler2.de",
            "website": "https://www.makler2.de",
            "rating": 4.5
        }
    ]
}
```

Laden Sie die Daten mit JavaScript:
```javascript
async function loadEntries() {
    const response = await fetch('data/makler.json');
    const data = await response.json();
    const grid = document.querySelector('.entries-grid');
    
    data.makler.forEach(makler => {
        const card = document.createElement('div');
        card.className = 'entry-card';
        card.dataset.category = makler.category.toLowerCase();
        card.innerHTML = `
            <div class="entry-image">
                <img src="${makler.image}" alt="${makler.name}">
            </div>
            <div class="entry-content">
                <h3>${makler.name}</h3>
                <p class="category">Kategorie: ${makler.category}</p>
                <p class="description">${makler.description}</p>
                <div class="entry-details">
                    <p><strong>Telefon:</strong> ${makler.phone}</p>
                    <p><strong>Email:</strong> ${makler.email}</p>
                    <p><strong>Website:</strong> <a href="${makler.website}" target="_blank">${makler.website}</a></p>
                </div>
                <div class="entry-footer">
                    <span class="rating">★★★★★ (${makler.rating})</span>
                </div>
            </div>
        `;
        grid.appendChild(card);
    });
}

loadEntries();
```

### Einträge bearbeiten

1. Finden Sie den Eintrag in `index.html` oder `data/makler.json`
2. Aktualisieren Sie die Informationen
3. Speichern Sie die Datei
4. Aktualisieren Sie den Browser (F5)

### Einträge löschen

1. Entfernen Sie den gesamten `entry-card` div-Block
2. Oder entfernen Sie das Objekt aus `makler.json`
3. Speichern und Browser aktualisieren

### Einträge sortieren

Fügen Sie Sortierfunktion zu `js/script.js` hinzu:
```javascript
function sortEntries(sortBy) {
    const cards = Array.from(document.querySelectorAll('.entry-card'));
    const grid = document.querySelector('.entries-grid');
    
    cards.sort((a, b) => {
        const aText = a.querySelector('h3').textContent;
        const bText = b.querySelector('h3').textContent;
        
        if (sortBy === 'name-asc') {
            return aText.localeCompare(bText);
        } else if (sortBy === 'name-desc') {
            return bText.localeCompare(aText);
        }
    });
    
    cards.forEach(card => grid.appendChild(card));
}
```

---

## Kategorien verwalten

### Kategorien definieren

Bearbeiten Sie die Kategorien in `js/script.js`:
```javascript
const categories = [
    { id: 'makler', name: 'Versicherungsmakler', color: '#667eea' },
    { id: 'unfall', name: 'Unfallversicherung', color: '#764ba2' },
    { id: 'kranken', name: 'Krankenversicherung', color: '#f093fb' },
    { id: 'leben', name: 'Lebensversicherung', color: '#4facfe' },
    { id: 'kfz', name: 'KFZ-Versicherung', color: '#00f2fe' },
    { id: 'haftung', name: 'Haftpflichtversicherung', color: '#43e97b' }
];
```

### Filter-Buttons erstellen

Fügen Sie zu `index.html` hinzu:
```html
<div class="filter-section">
    <button class="filter-btn active" data-filter="all">Alle</button>
    <button class="filter-btn" data-filter="makler">Versicherungsmakler</button>
    <button class="filter-btn" data-filter="unfall">Unfallversicherung</button>
    <button class="filter-btn" data-filter="kranken">Krankenversicherung</button>
    <button class="filter-btn" data-filter="leben">Lebensversicherung</button>
    <button class="filter-btn" data-filter="kfz">KFZ-Versicherung</button>
    <button class="filter-btn" data-filter="haftung">Haftpflichtversicherung</button>
</div>
```

### Filter-Funktionalität

Fügen Sie zu `js/script.js` hinzu:
```javascript
document.querySelectorAll('.filter-btn').forEach(btn => {
    btn.addEventListener('click', function() {
        const filter = this.dataset.filter;
        
        // Update active button
        document.querySelectorAll('.filter-btn').forEach(b => {
            b.classList.remove('active');
        });
        this.classList.add('active');
        
        // Filter entries
        const entries = document.querySelectorAll('.entry-card');
        entries.forEach(entry => {
            if (filter === 'all' || entry.dataset.category === filter) {
                entry.style.display = 'block';
            } else {
                entry.style.display = 'none';
            }
        });
    });
});
```

---

## Styling und Design

### Farben anpassen

Bearbeiten Sie die CSS-Variablen in `css/styles.css`:
```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
    --text-color: #333333;
    --light-bg: #f5f7fa;
    --border-color: #e0e0e0;
    --success-color: #43e97b;
    --warning-color: #fa7921;
    --danger-color: #ff6b6b;
}
```

### Layout anpassen

#### 3-Spalten Grid ändern
```css
.entries-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    margin: 40px 0;
}

/* Responsive: 2 Spalten auf Tablets */
@media (max-width: 768px) {
    .entries-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Responsive: 1 Spalte auf Mobilgeräten */
@media (max-width: 480px) {
    .entries-grid {
        grid-template-columns: 1fr;
    }
}
```

### Kartenstile anpassen

```css
.entry-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.entry-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 12px rgba(0, 0, 0, 0.15);
}
```

### Schriftarten ändern

Bearbeiten Sie `css/styles.css`:
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Inter:wght@400;500;600&display=swap');

body {
    font-family: 'Inter', sans-serif;
}

h1, h2, h3, h4, h5, h6 {
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
}
```

### Responsive Design anpassen

```css
/* Desktop */
@media (min-width: 1024px) {
    .entries-grid {
        grid-template-columns: repeat(3, 1fr);
    }
}

/* Tablet */
@media (min-width: 768px) and (max-width: 1023px) {
    .entries-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Mobile */
@media (max-width: 767px) {
    .entries-grid {
        grid-template-columns: 1fr;
    }
    
    .hero {
        height: 300px;
    }
    
    .entry-card {
        margin-bottom: 20px;
    }
}
```

---

## Erweiterte Anpassungen

### Header/Navigation anpassen

```html
<header class="header">
    <nav class="navbar">
        <div class="logo">
            <img src="images/logo.png" alt="Logo">
            <span>Versicherungsmakler Verzeichnis</span>
        </div>
        <ul class="nav-links">
            <li><a href="#home">Startseite</a></li>
            <li><a href="#directory">Verzeichnis</a></li>
            <li><a href="#about">Über uns</a></li>
            <li><a href="#contact">Kontakt</a></li>
        </ul>
    </nav>
</header>
```

### Footer hinzufügen

```html
<footer class="footer">
    <div class="footer-content">
        <div class="footer-section">
            <h4>Über uns</h4>
            <p>Das Versicherungsmakler Verzeichnis hilft Ihnen, die besten Makler zu finden.</p>
        </div>
        <div class="footer-section">
            <h4>Schnelllinks</h4>
            <ul>
                <li><a href="#">Datenschutz</a></li>
                <li><a href="#">Impressum</a></li>
                <li><a href="#">Nutzungsbedingungen</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <h4>Kontakt</h4>
            <p>Email: info@versicherungsmakler-verzeichnis.de</p>
            <p>Telefon: +49 (0) 123 456789</p>
        </div>
    </div>
    <div class="footer-bottom">
        <p>&copy; 2024 Versicherungsmakler Verzeichnis. Alle Rechte vorbehalten.</p>
    </div>
</footer>
```

### Meta-Tags für SEO

Bearbeiten Sie den `<head>` in `index.html`:
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Finden Sie die besten Versicherungsmakler in Ihrer Nähe. Vergleichen Sie Angebote und wählen Sie den perfekten Makler für Ihre Versicherungsbedürfnisse.">
    <meta name="keywords" content="Versicherungsmakler, Versicherungen, Makler vergleichen, Versicherungsberatung">
    <meta name="author" content="Versicherungsmakler Verzeichnis">
    <meta property="og:title" content="Versicherungsmakler Verzeichnis">
    <meta property="og:description" content="Die führenden Versicherungsmakler vergleichen">
    <meta property="og:image" content="images/og-image.jpg">
    <title>Versicherungsmakler Verzeichnis - Die führenden Versicherungsmakler vergleichen</title>
</head>
```

### Google Analytics hinzufügen

Fügen Sie vor dem schließenden `</head>`-Tag ein:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

---

## Fehlerbehebung

### Häufige Probleme und Lösungen

#### Problem: Bilder werden nicht angezeigt
**Lösung:**
- Überprüfen Sie, dass Bilddateien im `images/`-Verzeichnis vorhanden sind
- Überprüfen Sie Dateipfade in HTML (sollte `images/filename.jpg` sein)
- Stellen Sie sicher, dass Dateinamen korrekt geschrieben sind (Groß-/Kleinschreibung beachten)
- Überprüfen Sie Dateiberechtigungen

#### Problem: Suchfunktion funktioniert nicht
**Lösung:**
- Überprüfen Sie, dass `js/script.js` geladen wird
- Öffnen Sie Browser-Konsole (F12) auf Fehler
- Stellen Sie sicher, dass Suchbox-ID `searchBox` ist
- Überprüfen Sie, dass Eintragskarten-Klasse `entry-card` ist

#### Problem: Filter-Buttons funktionieren nicht
**Lösung:**
- Überprüfen Sie, dass `data-category` auf Einträgen gesetzt ist
- Überprüfen Sie, dass `data-filter` auf Buttons gesetzt ist
- Öffnen Sie Browser-Konsole auf JavaScript-Fehler
- Stellen Sie sicher, dass Klassennamen korrekt sind

#### Problem: Layout ist auf Mobilgeräten kaputt
**Lösung:**
- Überprüfen Sie Viewport-Meta-Tag: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Überprüfen Sie Media Queries in CSS
- Testen Sie mit Chrome DevTools Mobile-Ansicht
- Überprüfen Sie, dass CSS-Datei geladen wird

#### Problem: Website lädt langsam
**Lösungen:**
- Optimieren Sie Bilder (verwenden Sie TinyPNG oder ImageOptim)
- Minimieren Sie CSS und JavaScript
- Verwenden Sie CSS Grid statt Flexbox für bessere Performance
- Aktivieren Sie Gzip-Kompression auf dem Server
- Verwenden Sie CDN für externe Ressourcen

#### Problem: Suchmaschinen indexieren nicht
**Lösungen:**
- Erstellen Sie `sitemap.xml`
- Erstellen Sie `robots.txt`
- Übermitteln Sie Website zu Google Search Console
- Überprüfen Sie Meta-Tags
- Überprüfen Sie, dass Website nicht mit `noindex` gekennzeichnet ist

### Debugging-Tipps

1. **Browser-Konsole öffnen**: F12 oder Rechtsklick → Inspizieren
2. **Fehler überprüfen**: Schauen Sie auf der Console-Registerkarte nach roten Fehlern
3. **Netzwerk-Tab**: Überprüfen Sie, welche Dateien nicht geladen werden (404-Fehler)
4. **Elements-Tab**: Inspizieren Sie HTML-Struktur und CSS
5. **Responsive-Modus**: Testen Sie verschiedene Bildschirmgrößen

---

## Ressourcen und Support

### Dokumentation und Tutorials

- [MDN Web Docs](https://developer.mozilla.org/) - Umfassende HTML/CSS/JavaScript-Dokumentation
- [CSS-Tricks](https://css-tricks.com/) - CSS-Tipps und Tricks
- [W3Schools](https://www.w3schools.com/) - Anfänger-freundliche Tutorials
- [GitHub Docs](https://docs.github.com/) - GitHub Pages Dokumentation

### Tools und Ressourcen

- [Visual Studio Code](https://code.visualstudio.com/) - Code-Editor
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/) - Browser-Entwicklungstools
- [TinyPNG](https://tinypng.com/) - Bildoptimierung
- [Figma](https://www.figma.com/) - Design-Tool
- [Coolors](https://coolors.co/) - Farbpaletten-Generator

### Hosting-Anbieter

- [GitHub Pages](https://pages.github.com/) - Kostenlos
- [Netlify](https://www.netlify.com/) - Kostenlos mit Premium-Optionen
- [Vercel](https://vercel.com/) - Kostenlos mit Premium-Optionen
- [Bluehost](https://www.bluehost.com/) - Traditionelles Hosting
- [SiteGround](https://www.siteground.com/) - Traditionelles Hosting

### Domain-Registrare

- [GoDaddy](https://www.godaddy.com/)
- [Namecheap](https://www.namecheap.com/)
- [1&1](https://www.1und1.de/)
- [Strato](https://www.strato.de/)
- [Ionos](https://www.ionos.de/)

### Community und Support

- [Stack Overflow](https://stackoverflow.com/) - Fragen und Antworten
- [GitHub Issues](https://github.com/) - Bug-Reports und Feature-Requests
- [Reddit](https://www.reddit.com/r/web_design/) - Web-Design-Community
- [Dev.to](https://dev.to/) - Entwickler-Blog-Plattform

### Kontakt und Feedback

Haben Sie Fragen oder Feedback?
- **Email**: support@versicherungsmakler-verzeichnis.de
- **GitHub Issues**: [Repository Issues](https://github.com/yourusername/versicherungsmakler-verzeichnis/issues)
- **Twitter**: [@YourTwitterHandle](https://twitter.com/)

---

## Best Practices

### SEO-Optimierung
- Verwenden Sie aussagekräftige Meta-Beschreibungen
- Optimieren Sie Bilder mit Alt-Text
- Verwenden Sie semantisches HTML
- Erstellen Sie XML-Sitemap
- Verwenden Sie strukturierte Daten (Schema.org)

### Performance
- Minimieren Sie CSS und JavaScript
- Optimieren Sie Bilder
- Verwenden Sie Lazy Loading für Bilder
- Aktivieren Sie Browser-Caching
- Verwenden Sie CDN für statische Assets

### Sicherheit
- Verwenden Sie HTTPS
- Validieren Sie Benutzereingaben
- Verwenden Sie Content Security Policy (CSP)
- Halten Sie Abhängigkeiten aktuell
- Verwenden Sie CORS-Header korrekt

### Barrierefreiheit
- Verwenden Sie semantisches HTML
- Verwenden Sie ausreichend Farbkontrast
- Machen Sie Inhalte tastaturzugänglich
- Verwenden Sie ARIA-Labels
- Testen Sie mit Screen Readern

### Wartung
- Aktualisieren Sie Inhalte regelmäßig
- Überprüfen Sie auf kaputte Links
- Sichern Sie Ihre Website regelmäßig
- Überwachen Sie Analytics
- Führen Sie regelmäßige Backups durch

---

## Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert. Weitere Informationen finden Sie in der LICENSE-Datei.

---

## Versionsverlauf

### Version 1.0.0 (2024)
- Initiale Veröffentlichung
- 3-Spalten Grid Layout
- Basis-Suchfunktion
- Kategorie-Filter
- Responsive Design
- SEO-Optimierung

---

**Letzte Aktualisierung:** 2024
**Wartung:** Versicherungsmakler Verzeichnis Team

Vielen Dank, dass Sie das Versicherungsmakler Verzeichnis verwenden! Wir hoffen, dass diese Dokumentation Ihnen hilft, Ihre Website erfolgreich zu verwalten und anzupassen.