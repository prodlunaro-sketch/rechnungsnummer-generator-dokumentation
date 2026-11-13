# MCP mit Codex verbinden

Der Rechnungsnummer-MCP verbindet Codex mit deinen gespeicherten Nummernkreisen. Die Verbindung nutzt Streamable HTTP und meldet dich über Clerk an.

## In Codex Desktop einrichten

1. Öffne in Codex **Einstellungen → MCP-Server → Server hinzufügen**.
2. Wähle **Streamable HTTP**.
3. Vergib den Namen **Rechnungsnummer Generator**.
4. Trage diese Serveradresse ein: **https://api.rechnungsnummer-generator.de/mcp**
5. Speichere die Verbindung. Codex öffnet die OAuth-Anmeldung, wenn eine Anmeldung nötig ist.
6. Melde dich über Clerk an und prüfe die angefragten Berechtigungen, bevor du sie bestätigst.
7. Kehre zu Codex zurück und prüfe, ob die Rechnungsnummer-Werkzeuge in der Liste erscheinen.

Für einen ersten, nicht verändernden Test kannst du Codex fragen: „Welche Rechnungsnummer-Werkzeuge sind verfügbar?“

## Andere MCP-Clients

Wähle in deinem Client eine entfernte MCP-Verbindung mit Streamable HTTP und trage dieselbe Serveradresse ein. Schließe anschließend die OAuth-Anmeldung über Clerk ab.

## Was der MCP-Zugang kann

Der Server bietet eine Vorschau ohne Reservierung, das Auflisten und Anlegen von Nummernkreisen, das Reservieren der nächsten Nummern sowie das Archivieren eines Nummernkreises.

Eine Reservierung erhöht den Zähler dauerhaft und kann nicht rückgängig gemacht werden. Lass dir vor dem Anlegen, Reservieren oder Archivieren die geplante Änderung anzeigen und bestätige sie erst, wenn sie stimmt. Der MCP-Zugriff kann Daten deines angemeldeten Kontos lesen oder ändern.

Der MCP-Zugang braucht ein Konto. Eine API-Vorschau ohne Anmeldung gibt es unter [Rechnungsnummer-API](api.md).