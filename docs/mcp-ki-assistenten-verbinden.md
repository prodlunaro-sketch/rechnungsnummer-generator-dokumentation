# Rechnungsnummer-MCP mit KI-Assistenten verbinden

Mit dem MCP-Server können KI-Assistenten auf die Nummernkreise deines Kontos zugreifen. Die Verbindung nutzt Streamable HTTP und OAuth über Clerk.

**Serveradresse:** https://api.rechnungsnummer-generator.de/mcp

Für Kontoaktionen brauchst du ein Konto. Gib keine Zugangsdaten an deinen Assistenten weiter. Melde dich ausschließlich im OAuth-Fenster an und prüfe die angefragten Berechtigungen.

## Codex Desktop und Codex CLI

1. Öffne in Codex **Einstellungen → MCP-Server → Server hinzufügen**.
2. Wähle **Streamable HTTP** und trage einen Namen sowie die Serveradresse ein.
3. Speichere den Server. Wenn Codex danach fragt, wähle **Authentifizieren** und melde dich bei Clerk an.
4. Prüfe in Codex, ob die Rechnungsnummer-Werkzeuge angezeigt werden.

Die Codex-App, Codex CLI und die Erweiterung verwenden dieselbe MCP-Konfiguration. [Codex-Anleitung von OpenAI](https://learn.chatgpt.com/docs/extend/mcp?surface=cli)

## ChatGPT

Eigene MCP-Apps und Schreibaktionen werden je nach Tarif und Arbeitsbereich angeboten. Falls der Entwicklermodus in deinem Konto verfügbar ist:

1. Öffne die Einstellungen des Arbeitsbereichs und aktiviere den Entwicklermodus.
2. Lege unter den MCP-Apps beziehungsweise Connectors eine eigene Verbindung an.
3. Trage die Serveradresse ein und verbinde dein Konto über Clerk.

[ChatGPT: Entwicklermodus und MCP-Apps](https://help.openai.com/en/articles/12584461-developer-mode-and-full-mcp-connectors-in-chatgpt-beta)

## Claude und Claude Desktop

1. Öffne **Einstellungen → Connectors**.
2. Wähle **Eigenen Connector hinzufügen** und trage die Serveradresse ein.
3. Wähle **Verbinden**, melde dich bei Clerk an und prüfe die Berechtigungen.

Entfernte MCP-Connectoren können je nach Claude-Tarif verfügbar sein. [Offizielle Anleitung von Anthropic](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp)

## Gemini CLI

Füge den entfernten HTTP-Server hinzu:

```sh
gemini mcp add --transport http --scope user rechnungsnummer https://api.rechnungsnummer-generator.de/mcp
```

Starte Gemini CLI. Öffne `/mcp` und nutze bei Bedarf `/mcp auth rechnungsnummer`, um Clerk-OAuth abzuschließen.

[Offizielle Gemini-CLI-Dokumentation](https://github.com/google-gemini/gemini-cli/blob/main/docs/tools/mcp-server.md)

## Cursor

Öffne in Cursor die MCP-Einstellungen, füge einen entfernten HTTP-Server hinzu und trage die Serveradresse ein. Schließe die OAuth-Anmeldung ab, falls Cursor danach fragt.

[Offizielle MCP-Dokumentation für Cursor](https://docs.cursor.com/context/model-context-protocol)

## Visual Studio Code mit GitHub Copilot

1. Wähle den Befehl **Chat: Anpassungen öffnen** und öffne **MCP-Server**.
2. Wähle **Server hinzufügen → HTTP** und füge die Serveradresse ein.
3. Schließe die Anmeldung im Browser ab.

[Offizielle MCP-Anleitung für VS Code](https://code.visualstudio.com/docs/copilot/chat/mcp-servers)

## Werkzeuge und Auswirkungen

Der Server kann eine Vorschau erstellen, Nummernkreise auflisten oder anlegen, Nummern reservieren und Nummernkreise archivieren.

Eine Reservierung erhöht den Zähler dauerhaft. Sie lässt sich nicht rückgängig machen. Bitte deinen Assistenten, dir vor dem Anlegen, Reservieren oder Archivieren zu erklären, was er ändern will, und bestätige die Aktion erst danach.

MCP und API-Schlüssel teilen sich das monatliche Kontingent des Kontos. Die öffentliche REST-Vorschau benötigt kein Konto und reserviert keine Nummern: [API-Anleitung](api.md).

Die Website-Anleitung mit weiteren Hinweisen steht unter [rechnungsnummer-generator.de/api/mcp](https://rechnungsnummer-generator.de/api/mcp).
