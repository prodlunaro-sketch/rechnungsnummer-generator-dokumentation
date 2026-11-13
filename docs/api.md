# REST-API für Rechnungsnummern

Die öffentliche Vorschau-API erstellt eine Liste fortlaufender Rechnungsnummern. Sie ist ohne Anmeldung und API-Schlüssel nutzbar.

## Endpunkt

**Methode:** POST  
**Adresse:** https://api.rechnungsnummer-generator.de/v1/numbers/preview  
**Inhaltstyp:** application/json

## Eingaben

| Feld | Bedeutung | Erlaubte Werte |
| --- | --- | --- |
| prefix | Optionales Präfix | leer, RE, RG oder INV |
| dateFormat | Datumsbestandteil | YYYY, YYYY-MM oder none |
| separator | Trennzeichen | Bindestrich, Schrägstrich oder Punkt |
| startNumber | Erste laufende Nummer | Ganze Zahl ab 1 |
| count | Anzahl der Nummern | 1 bis 100 |
| padding | Stellenzahl mit führenden Nullen | 1 bis 12 |
| date | Optionales Datum | Kalenderdatum im Format JJJJ-MM-TT |

## Antwort und Grenzen

Die Antwort enthält die erzeugten Nummern unter „data.numbers“ und meldet in den Metadaten „reserved: false“. Die Vorschau speichert keine Liste, reserviert keine Nummern und führt kein Register bereits vergebener Rechnungsnummern. Prüfe deshalb selbst, ob die Nummern in deinem Rechnungssystem noch frei sind.

Pro IP-Adresse sind höchstens 30 Anfragen pro Minute möglich. Eine ungültige Eingabe führt zu HTTP 400, eine zu große Anfrage zu HTTP 413 und ein überschrittenes Limit zu HTTP 429. Bei HTTP 429 hilft der Retry-After-Hinweis im Antwortkopf.

Für Kontofunktionen wie gespeicherte Nummernkreise und dauerhafte Reservierungen ist eine Anmeldung erforderlich. Die MCP-Einrichtung steht in [MCP mit Codex verbinden](mcp-mit-codex-verbinden.md).