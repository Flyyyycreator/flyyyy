# 🛠️ Admin Events System - Bedienungsanleitung

## Überblick

Das Admin Events System erlaubt Administratoren, Spielern verschiedene Belohnungen zu verteilen und Admin-Events zu erstellen. Dies kann entweder an einzelne Spieler oder als Broadcast an alle Spieler erfolgen.

## Zugriff auf Admin Events

1. **Admin-Panel öffnen**: Klicke auf 🛠️ ADMIN im Login-Screen
2. **Admin-Code eingeben**: Gib `Flyyyy-Admin-7391-X` ein und klicke "AKTIVIEREN"
3. **Events-Tab öffnen**: Im Admin-Panel auf den 🎁 **EVENTS** Tab klicken

## Verfügbare Reward-Typen

### 1. 🪙 Coins
- **Beschreibung**: Geldbelohnung
- **Einstellung**: Anzahl der Coins eingeben (z.B. 500, 1000, etc.)
- **Anwendung**: Sofort auf dem Spieler-Account gutgeschrieben

### 2. 👾 Skins
- **Beschreibung**: Character-Designs freischalten
- **Verfügbare Skins**:
  - Bird (Standard)
  - Voltfrog
  - StormOwl
  - Astrion
  - und weitere...
- **Anwendung**: Zum Inventar des Spielers hinzugefügt

### 3. 🌍 Welten (Worlds)
- **Beschreibung**: Neue Spielwelten freischalten
- **Verfügbare Welten**:
  - Gizeh (Standard)
  - Atlantis
  - Mars
  - Tokyo
  - und weitere...
- **Anwendung**: Zum Welt-Inventar hinzugefügt

### 4. 🎵 Sounds
- **Beschreibung**: Neue Sound-Sets freischalten
- **Verfügbare Sounds**:
  - Classic (Standard)
  - Arcade
  - Laser
  - Bubble
  - Power
- **Anwendung**: Zum Sound-Inventar hinzugefügt

### 5. 🎡 Lucky Wheel Spins
- **Beschreibung**: Drehungen am Glücksrad
- **Optionen**:
  - 1 Spin
  - 5 Spins
  - 10 Spins
- **Anwendung**: Zur Lucky Wheel Spin-Anzahl hinzugefügt

## Event-Erstellung Schritt für Schritt

### Event an einzelnen Spieler senden:

```
1. Reward-Typ auswählen (z.B. "🪙 Coins")
2. Coins-Anzahl eingeben (z.B. 500)
3. Empfänger-E-Mail oder UID eingeben
4. (Optional) Nachricht hinzufügen
5. "✅ EVENT ERSTELLEN" klicken
```

### Broadcast-Event an alle Spieler:

```
1. Reward-Typ auswählen (z.B. "👾 Skin")
2. Skin auswählen (z.B. "Voltfrog")
3. "📢 BROADCAST" Button klicken (wird grün/aktiv)
4. (Optional) Nachricht hinzufügen
5. "✅ EVENT ERSTELLEN" klicken
```

### Event zurücksetzen:
Klicke "ZURÜCKSETZEN", um alle Felder zu löschen und von vorne zu beginnen.

## Event-Status

Jedes erstellte Event zeigt seinen Status:

- ✅ **OK**: Event erfolgreich erstellt
- 🔄 **PENDING**: Event wird gerade verarbeitet
- ❌ **FEHLER**: Event konnte nicht erstellt werden

## Event-Verlauf

Die letzten 10 erstellten Events sind im Bereich "✅ Zuletzt erstellte Events" sichtbar.

Jeder Event-Eintrag zeigt:
- Reward-Typ und Menge
- Empfänger (einzelner Spieler oder "📢 ALLE SPIELER")
- Erstellungs-Datum und Admin
- Optionale Nachricht
- Status (OK / FEHLER / PENDING)

## Beispiele

### Beispiel 1: Willkommens-Event
```
Type: 🪙 Coins
Amount: 100
Recipient: spieler@example.com
Message: Willkommen im Spiel! Hier sind 100 Coins zum Start.
Result: Der Spieler erhält 100 Coins
```

### Beispiel 2: Neuer Skin Freischaltung
```
Type: 👾 Skin
Item: Voltfrog
Recipient: [Broadcast aktiv]
Message: Neuer Skin "Voltfrog" für alle Spieler freigeschaltet!
Result: Alle online Spieler erhalten den Voltfrog Skin
```

### Beispiel 3: Lucky Wheel Gewinn
```
Type: 🎡 Lucky Wheel Spins
Item: 5 Spins
Recipient: glücklicher-spieler@example.com
Message: Gewinner der Wochenende-Verlosung!
Result: Der Spieler erhält 5 zusätzliche Lucky Wheel Spins
```

### Beispiel 4: Neue Welt für alle
```
Type: 🌍 Welt
Item: Mars
Recipient: [Broadcast aktiv]
Message: Neue Welt "Mars" ist jetzt für alle verfügbar!
Result: Alle Spieler erhalten Zugriff auf die Mars-Welt
```

## Wichtige Hinweise

⚠️ **Firebase Verbindung**:
- Events für einzelne Spieler benötigen eine aktive Firebase-Verbindung
- Wenn Firebase nicht verfügbar ist, wird das Event lokal gespeichert
- Das Event wird nicht auf den Spieler-Account übertragen

⚠️ **Broadcast Events**:
- Broadcast-Events werden an ALLE registrierten Spieler gesendet
- Nutze dies mit Bedacht!
- Events werden nacheinander verarbeitet (kann bei vielen Spielern länger dauern)

⚠️ **Event-Speicherung**:
- Alle Events werden lokal im Browser gespeichert
- Events sind persistent und werden über Browser-Neuladen erhalten
- Beim Löschen des Browser-Speichers gehen die Events verloren

## Fehlerbehandlung

Wenn ein Event fehlschlägt:

1. **Spieler nicht gefunden**: Überprüfe die E-Mail/UID
2. **Firebase nicht verfügbar**: Überprüfe die Internetverbindung
3. **Permissions Error**: Stelle sicher, dass Admin-Rechte aktiv sind

---

**Version**: 1.0 | **Datum**: August 2026 | **Admin System**: FLYYYY 2.9.2
