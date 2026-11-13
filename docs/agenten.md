# Rechnungsnummer Generator mit Coding-Agenten nutzen

Diese Anleitung passt für Codex, Claude Code, Gemini CLI, Cursor, GitHub Copilot und andere Coding-Agenten.

## Wofür welche Verbindung gedacht ist

- **REST-API:** Erzeugt eine unverbindliche Nummernliste ohne Anmeldung und API-Schlüssel. Nummern werden nicht gespeichert oder reserviert.
- **MCP:** Verbindet einen Assistenten mit den Nummernkreisen eines angemeldeten Kontos. Nummern können dauerhaft reserviert werden.

Der REST-Endpunkt lautet `POST https://api.rechnungsnummer-generator.de/v1/numbers/preview`. Details zu Feldern, Limits und Antworten stehen in der [API-Anleitung](api.md).

## Agenten vorbereiten

1. Öffne die [Anleitung für Agenten auf der Website](https://rechnungsnummer-generator.de/agenten).
2. Kopiere dort die Anweisung in den Coding-Agenten.
3. Lass ihn zuerst das vorhandene Projekt und dessen Anweisungen prüfen.
4. Prüfe den vorgeschlagenen Ablauf, bevor du Codeänderungen oder Kontoaktionen freigibst.

Die Anweisung unterscheidet zwischen der REST-Vorschau und MCP-Aktionen. Sie weist den Agenten an, keine API-Schlüssel oder Kundendaten ins Frontend einzubauen und vor dauerhaften Änderungen nachzufragen.

## MCP-Verbindung einrichten

Folge der passenden Einrichtungsanleitung für deinen Client unter [MCP mit KI-Assistenten verbinden](mcp-ki-assistenten-verbinden.md). Der Server verwendet OAuth über Clerk. Erfinde keine Zugangsdaten und gib dein Passwort nicht in den Chat ein.

Eine Nummernreservierung erhöht den Zähler und lässt sich nicht zurücknehmen. Bitte den Agenten, die konkrete Reihe und die nächste Nummer zu nennen, bevor er reserviert.

## Hinweis zu vertraulichen Daten

Die Vorschau-API braucht keine Kunden- oder Rechnungsdaten. Übermittle keine vertraulichen Inhalte an den Agenten oder MCP-Server, wenn sie für die Aufgabe nicht erforderlich sind.
