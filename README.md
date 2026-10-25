# codingrandolph.github.io

Öffentliche Webseite zur App **Adventskalender** (GitHub Pages). Der Quellcode der App
liegt nicht hier; dieses Repo enthält nur, was öffentlich sein muss:

| Pfad | Zweck |
|---|---|
| `/` | Kurze Vorstellung der App |
| `/support/` | Support-URL für App Store Connect (Kontakt + FAQ) |
| `/datenschutz/` | Datenschutz-URL für App Store Connect |
| `/gift/?t=<Schlüssel>` | Ziel der Geschenk-Links; mit installierter App öffnet iOS direkt die App (Universal Link), sonst diese Seite mit App-Store-Link |
| `/.well-known/apple-app-site-association` | Universal-Link-Freigabe für `DM5AT74F4W.codingrandolph.Adventskalender`, Pfade `/gift/*` |

`.nojekyll` sorgt dafür, dass GitHub Pages den Ordner `.well-known` ausliefert.

## Noch offen

- `APP_STORE_URL` in `gift/index.html` durch den Link zur App ersetzen, sobald sie im
  App Store ist (bis dahin ist der Knopf „App laden“ ausgeblendet).
- Datenschutzerklärung bei Änderungen an der App anpassen und das „Stand“-Datum erneuern.

## Einrichtung

1. GitHub-Organisation `codingrandolph` (Free) anlegen.
2. Öffentliches Repo `codingrandolph/codingrandolph.github.io` anlegen und diesen Ordner pushen.
3. Repo-Einstellungen → Pages → Branch `main`, Ordner `/` (root).
4. Prüfen: `https://codingrandolph.github.io/.well-known/apple-app-site-association` liefert das JSON.
