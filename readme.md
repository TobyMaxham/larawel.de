# Es heißt Laravel.

Eine völlig unnötige, aber sehr notwendige Korrektur-Website für ein PHP-Framework, dessen Name im Team-Chat konsequent falsch geschrieben wird.

![Es heißt Laravel. Nicht Larawelz. Nicht Larawels.](https://larawelz.de/assets/og-image.png)

## Worum geht's

Kollegen haben angefangen, "Laravel" konsequent als **Larawelz**, **Larawels** und (neuerdings) **Larawel** zu schreiben — in Branch-Namen, Commit-Messages und im Daily-Chat. Diese Seite ist die offizielle, komplett unseriöse Gegenreaktion.

## Domains

| Domain               | Zweck                                                                          |
|----------------------|--------------------------------------------------------------------------------|
| `larawelz.de`        | Hauptseite                                                                     |
| `larawels.de`        | Spiegelt dieselbe Hauptseite, personalisiert per JS auf die jeweilige Variante |
| `larawel.de`         | Dritte Variante (v→w vertauscht), ebenfalls gespiegelt                         |
| `status.larawelz.de` | Fake-Statuspage im Uptime-Monitoring-Stil                                      |

Alle drei Haupt-Domains liefern dieselben Dateien aus, die Personalisierung passiert clientseitig
über `window.location.hostname` — kein Server-Branching, kein PHP nötig.

## Struktur

```
./public
├── index.html                    # Hauptseite: Diff-Hero, Wanted-Karten, PR-Mock, Git-Beweise, Aussprache
├── woerterbuch.html              # Duden-Stil-Eintrag: Deklination, Genitiv-Erklärung, Falschschreibungen
├── status.html                   # Fake-Statuspage: Komponenten, Uptime-Streifen, Incident-Historie
├── 404.html                      # Custom 404, thematisch passend
└── assets/
    ├── og-image.png              # OG-Bild Hauptseite (1200×630)
    ├── og-image-woerterbuch.png  # OG-Bild Wörterbuch (1200×630)
    └── og-image-status.png       # OG-Bild Statuspage (1200×630)
```

## Features

- **Diff-Hero**: animierter Git-Diff, der die Falschschreibungen live durchstreicht und korrigiert
- **Domain-Personalisierung**: erkennt exakt (nicht per Substring), auf welcher der drei Domains die Seite läuft, und hebt die passende "Wanted"-Karte hervor
- **Aussprache**: Web-Speech-API-Button (`speechSynthesis`) mit aktiver Auswahl der besten verfügbaren Systemstimme, plus Link zu einem externen IPA-Reader als Fallback
- **Wörterbucheintrag**: eigene Unterseite im Print-Dictionary-Look, inkl. Genitiv-Insider ("des Laravels")
- **Statuspage**: eigene Subdomain, Uptime-Verlauf pro Begriff, Incident-Historie
- **OG/SEO**: vollständige Open-Graph- und Twitter-Card-Tags pro Seite, für saubere Vorschauen in Teams/Slack


## Lizenz

MIT — mit einer Ausnahme: die Begriffe "Larawelz", "Larawels" und "Larawel" dürfen unter keinen
Umständen weiterverwendet, zitiert oder in Branch-Namen kopiert werden.
Bei Zuwiderhandlung: siehe [`/woerterbuch`](https://larawelz.de/woerterbuch).

## Kontakt

Für Widerspruch, Beschwerden oder den hartnäckigen Glauben, es hieße doch anders:
**info@larawelz.de**

Antwortzeit variiert je nach Tonfall der Nachricht.


## Ton-Hinweis

Alles auf dieser Seite ist bewusst overdramatisch und dient ausschließlich der
internen Belustigung. Es gibt keine echten Vorfälle, keine echten Namen,
keine echte Statusüberwachung — nur ein Framework, das richtig heißt.
