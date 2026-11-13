# Rechnungsnummer Generator

Wir stellen einen kostenlosen Generator für Rechnungsnummern, eine öffentliche REST-API und einen MCP-Server bereit. Diese Sammlung erklärt, wie die Angebote funktionieren und wie du sie mit deinem eigenen Ablauf verbindest.

## Angebote

### Rechnungsnummern im Browser erstellen

Öffne den [Rechnungsnummer Generator](https://rechnungsnummer-generator.de/). Die Liste entsteht direkt im Browser; für die einfache Erstellung brauchst du kein Konto.

### REST-API

Die Vorschau-API erstellt eine Nummernliste ohne Anmeldung und API-Schlüssel. Sie speichert und reserviert keine Nummern. Pro Anfrage sind bis zu 100 Nummern möglich; pro IP-Adresse gelten höchstens 30 Anfragen je Minute.

Der Endpunkt lautet: **POST https://api.rechnungsnummer-generator.de/v1/numbers/preview**

Die Eingaben und die Antwort sind in der [API-Anleitung](docs/api.md) beschrieben.

### MCP für KI-Assistenten

Mit dem MCP-Server kann ein angemeldeter MCP-Client auf die Kontofunktionen zugreifen. Die Verbindung verwendet OAuth über Clerk und braucht ein Konto. Der Server unterstützt das Anzeigen und Anlegen von Nummernkreisen, eine unverbindliche Vorschau, das Reservieren von Nummern und das Archivieren von Reihen.

Die Serveradresse lautet: **https://api.rechnungsnummer-generator.de/mcp**

Einrichtungswege für ChatGPT, Codex, Claude, Gemini CLI, Cursor und GitHub Copilot stehen in [MCP mit KI-Assistenten verbinden](docs/mcp-ki-assistenten-verbinden.md). Die bisherige [Codex-Kurzanleitung](docs/mcp-mit-codex-verbinden.md) bleibt ebenfalls verfügbar.

### Agenten

Eine fertige Anleitung für Coding-Agenten erklärt die REST-API, MCP und vorsichtige Freigaben: [Agenten einrichten](docs/agenten.md). Die gleiche Anleitung steht auch auf der [Website](https://rechnungsnummer-generator.de/agenten).

## Worum es in diesem Repository geht

Dieses öffentliche Repository enthält Anleitungen und Hintergrundinformationen. Es enthält keinen Programmcode, keine SDKs, keine Zugangsdaten und keine Kundendaten. Der Quellcode der Website und der Dienste bleibt in privaten Repositories.

## Warum der Quellcode geschlossen bleibt

Wir möchten selbst dafür sorgen, dass Generator, API und MCP kostenlos erreichbar bleiben. Ein öffentlich kopierter Dienst könnte mit einer Bezahlschranke weitergeführt werden. Dazu kommen laufende Aufgaben wie Fehlermeldungen prüfen, Änderungen anderer Entwickler bewerten, Anleitungen pflegen und Fragen beantworten. Diese Arbeit soll nicht die Zeit für die Produktentwicklung aufbrauchen.

Offener Quellcode kann durch zusätzliche Prüfungen helfen, Schwachstellen zu finden. Er macht den Code zugleich für gezielte Suche nach Fehlern sichtbar. Das allein macht geschlossenen Code nicht automatisch sicherer; Zugangsdaten und Server müssen in jedem Fall geschützt werden. Wir behalten den Code außerdem lieber unter eigener Kontrolle, damit wir unerwünschte Einsatzbereiche ablehnen können, darunter militärische Nutzung.

Mehr dazu steht in [Warum der Quellcode geschlossen bleibt](docs/warum-der-quellcode-geschlossen-bleibt.md).

## Rückmeldung

Ideen und Fehlerberichte kannst du über das [Kontaktformular](https://rechnungsnummer-generator.de/kontakt) senden.

## Projekt- und Profilseiten

- [Website](https://rechnungsnummer-generator.de/)
- [Bluesky](https://bsky.app/profile/rechnungen.bsky.social)
- [Mastodon](https://mastodon.social/@rechnungen)
- [X](https://x.com/rechnungende)
