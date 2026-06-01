# NexusControl

Die Desktop-Begleit-App für die **[ЯHP]**-Allianz.

NexusControl ist eine einzelne, in sich geschlossene Windows-Anwendung. Es gibt **keinen Installer**, es werden **keine Administratorrechte** benötigt, und alles Nötige ist bereits enthalten. Du lädst eine einzige Datei herunter, legst sie in einen Ordner deiner Wahl und startest sie — alles Weitere legt die App beim ersten Start selbst an.

---

## Voraussetzungen

- **Windows 10 oder 11, 64-Bit.**
- Eine **Internetverbindung**.
- Ein **Discord-Konto**, das Mitglied im **[ЯHP]**-Server ist (welche Inhalte du siehst, hängt von deinen Discord-Rollen ab).
- Keine .NET-Installation nötig — die Laufzeitumgebung steckt bereits in der EXE.

---

## Installation

1. **Lade** die neueste `NexusControl.exe` von der **Releases**-Seite des Projekts herunter.
2. **Lege einen Ordner** an einem beschreibbaren Ort an, z. B.:
   - `C:\Tools\NexusControl`  oder  `D:\NexusControl`
   - Vermeide `C:\Programme\…` — dieser Ort ist schreibgeschützt, die App muss aber ihre eigenen Dateien neben der EXE anlegen.
3. **Verschiebe** `NexusControl.exe` in diesen Ordner.
4. **Starte** die App per Doppelklick.

Das war's. Beim **ersten Start** legt NexusControl automatisch einen `data`-Unterordner neben der EXE an und befüllt ihn mit allem Nötigen (Einstellungen, Logs usw.). Du musst nichts einrichten.

```
NexusControl\
├─ NexusControl.exe      ← die App (die einzige Datei, die du herunterlädst)
└─ data\                 ← wird beim ersten Start automatisch erzeugt
   ├─ config.json
   ├─ logs\
   └─ … (weitere Dateien, die die App selbst verwaltet)
```

> **Windows-SmartScreen-Warnung beim ersten Start.**
> Da die App nicht mit einem (kostenpflichtigen) Code-Signing-Zertifikat signiert ist, zeigt Windows evtl. *„Der Computer wurde durch Windows geschützt"*. Das ist normal.
> Einmal auf **Weitere Informationen → Trotzdem ausführen** klicken. Windows merkt sich die Entscheidung für diese Datei.

---

## Erster Start & Anmeldung

1. Nach dem Start auf **„Sign in with Discord"** klicken.
2. Die App im Browser autorisieren.
3. Fertig. Welche Tabs und Daten du siehst, hängt von deinen Discord-Rollen im **[ЯHP]**-Server ab.

Deine Anmeldung wird **verschlüsselt** im `data\`-Ordner gespeichert und ist an dein Windows-Benutzerkonto gebunden — sie lässt sich nicht einfach auf einen anderen PC oder Benutzer kopieren.

---

## Updates

NexusControl **prüft bei jedem Start automatisch auf eine neuere Version**. Ist eine verfügbar, fragt die App nach; nach Bestätigung lädt sie die neue Version, ersetzt sich selbst und startet neu. Du musst nichts manuell herunterladen.

Falls du doch von Hand aktualisieren willst: einfach die neueste `NexusControl.exe` von der Releases-Seite laden und die alte im Ordner überschreiben. Dein `data`-Ordner bleibt unangetastet.

---

## Verschieben oder sichern

Die App ist vollständig **portabel**. Zum Verschieben auf einen anderen Ordner/ein anderes Laufwerk einfach den **gesamten** `NexusControl`-Ordner (die `.exe` **und** den `data`-Ordner) zusammen verschieben. Zum Sichern deiner Einstellungen den `data`-Ordner kopieren.

> Hinweis: Das verschlüsselte Anmelde-Token ist an deinen Windows-Benutzer gebunden. Auf einem **anderen PC oder Windows-Konto** wirst du einfach erneut zur Anmeldung aufgefordert — alles andere funktioniert.

---

## Deinstallieren

Es gibt nichts zu deinstallieren. **Lösche den `NexusControl`-Ordner** und die App ist samt allen Daten weg.

---

## Problembehebung

- **„Der Computer wurde durch Windows geschützt" (SmartScreen):** auf *Weitere Informationen → Trotzdem ausführen* klicken (siehe oben).
- **Virenscanner meldet die Datei:** in sich geschlossene, unsignierte Single-File-Apps werden gelegentlich fälschlich erkannt. Nur von der offiziellen Releases-Seite laden; bei Bedarf eine Ausnahme für den Ordner hinzufügen.
- **App legt keine Dateien an / Fehler beim Start:** sicherstellen, dass der Ordner **beschreibbar** ist (nicht `Programme`, kein schreibgeschützter Ort). Ordner z. B. nach `C:\Tools\NexusControl` legen und erneut versuchen.
- **Keine Daten / Tabs fehlen nach der Anmeldung:** normal, wenn deine Discord-Rollen keinen Zugriff geben — prüfe deine Rollen im **[ЯHP]**-Server.
- **Zurücksetzen:** App schließen und den `data`-Ordner löschen. Er wird beim nächsten Start sauber neu erzeugt (du musst dich dann erneut anmelden).
- **Logs** für den Support liegen in `data\logs\`.

---

*NexusControl ist ein internes Tool der [ЯHP]-Allianz. Bitte die EXE nicht außerhalb der Allianz weitergeben.*
