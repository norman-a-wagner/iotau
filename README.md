# Norman Wagner — Scientific Works (Website)

Statische Webseite mit dem wissenschaftlichen Werk von Dr. rer. nat. Norman Wagner.
Reines HTML/CSS/JS, keine Build-Schritte, kein Server nötig — lässt sich direkt über **GitHub Pages** veröffentlichen.

## Dateien im Repository

| Datei | Zweck | Pflicht |
|---|---|---|
| `index.html` | Hauptseite (Profil + Publikationsliste mit Suche/Filter) | ✅ |
| `pass04.gif` | Porträtfoto im Kopfbereich | ✅ |
| `ORCID-iD_icon_32x32.png` | ORCID-Icon | ✅ |
| `collaboration-network.html` | Interaktives Koautoren-Netzwerk (optional) | ⬜ |
| `collaboration-worldmap.html` | Kooperations-Weltkarte (optional) | ⬜ |
| `EuclidCircularA-*.woff2` | Lizenzierte Schriftdateien (optional, siehe unten) | ⬜ |

> Alle drei Pflichtdateien müssen **im selben Ordner** liegen, damit Foto, Icon und relative Links funktionieren.

## Schnellstart (über die GitHub-Weboberfläche, ohne Git-Kenntnisse)

1. Bei <https://github.com> einloggen und oben rechts **„+“ → „New repository“** wählen.
2. Repository benennen:
   - für eine **persönliche Hauptseite**: exakt `DEINBENUTZERNAME.github.io`
   - oder für eine **Projektseite**: ein beliebiger Name, z. B. `scientific-works`
   Sichtbarkeit **Public**, dann **Create repository**.
3. **„uploading an existing file“** anklicken und die Dateien aus diesem Ordner hochladen
   (mindestens `index.html`, `pass04.gif`, `ORCID-iD_icon_32x32.png`), dann **Commit changes**.
4. Im Repository: **Settings → Pages**.
5. Unter **Build and deployment → Source: „Deploy from a branch“**, Branch **`main`**, Ordner **`/ (root)`**, **Save**.
6. Nach ein bis zwei Minuten ist die Seite erreichbar unter:
   - persönliche Seite: `https://DEINBENUTZERNAME.github.io/`
   - Projektseite: `https://DEINBENUTZERNAME.github.io/scientific-works/`

`index.html` wird automatisch als Startseite ausgeliefert. HTTPS ist bei GitHub Pages automatisch aktiv.

## Alternative: per Git (Kommandozeile)

```bash
git init
git add index.html pass04.gif ORCID-iD_icon_32x32.png \
        collaboration-network.html collaboration-worldmap.html
git commit -m "Add website"
git branch -M main
git remote add origin https://github.com/DEINBENUTZERNAME/REPONAME.git
git push -u origin main
```

Danach wie oben unter **Settings → Pages** den Branch `main` / Ordner `/ (root)` aktivieren.

## Schriftart Euclid (optional)

Die Seite verwendet **Euclid** und fällt sonst sauber auf **Times New Roman** zurück.
Wenn du die lizenzierten Schriftdateien hast, lege sie in denselben Ordner:

```
EuclidCircularA-Regular.woff2
EuclidCircularA-Medium.woff2
EuclidCircularA-SemiBold.woff2
EuclidCircularA-Bold.woff2
EuclidCircularA-MediumItalic.woff2
```

Ohne diese Dateien bleibt die Seite voll funktionsfähig (Serifen-Ersatzschrift).

## Verlinkte PDFs / Volltexte

Einige Publikationen verlinken auf lokale PDFs mit **relativen** Pfaden
(z. B. `2021_Schmidt_ISEMA_Proc_O.pdf`, `WagnerDGG2008.pdf`, `ISEMA_Proceedings_2009.pdf`).
Diese funktionieren nur, wenn du die entsprechenden PDF-Dateien **ebenfalls ins Repository** legst.
Links mit voller Adresse (`http://www.hy-dra.de/...`, DOI, arXiv) funktionieren ohne weiteres Zutun.

## Zusatzseiten (Netzwerk & Weltkarte)

`collaboration-network.html` und `collaboration-worldmap.html` laden ihre Bibliotheken
(D3, TopoJSON) von einem CDN — sie benötigen also eine Internetverbindung beim Aufruf.
Du kannst sie z. B. aus `index.html` verlinken, falls gewünscht.

## Eigene Domain (optional)

Unter **Settings → Pages → Custom domain** lässt sich z. B. `www.hy-dra.de` eintragen
(zusätzlich ein DNS-CNAME beim Domain-Anbieter auf `DEINBENUTZERNAME.github.io` setzen).

---
© Norman Wagner — scientific works
