# DATEV-HTML-Tools

Kleine Werkzeuge für die Buchhaltung mit **DATEV Rechnungswesen**. Jedes Tool ist eine einzelne
HTML-Datei: herunterladen, im Browser öffnen, fertig. Keine Installation, kein Konto, keine Cloud.

Die Tools stammen aus den YouTube-Videos von Andreas Hausmann (AHA Consulting GmbH) und werden
hier kostenlos bereitgestellt.

> **Bitte zuerst lesen:** Die Tools werden ohne Support bereitgestellt
> ([Kein Support](#kein-support)). Prüfen Sie jedes Ergebnis fachlich, bevor Sie es in DATEV
> weiterverarbeiten ([Wichtige Hinweise](#wichtige-hinweise)).

---

## Die Tools

| Tool | Wofür | Schreibt in DATEV? | Datei |
|---|---|---|---|
| **Klärungs-Tool** | Gleicht ein Klärungskonto mit den offenen Posten der Kreditoren ab. Buchungen, die sich über Belegfeld 1 ausgleichen, blendet es aus. Markierte Buchungen übergibt es als Storno und Neubuchung im Buchungsstapel. Für die übrigen erstellt es eine Beleganforderung per E-Mail an den Mandanten. | ja, als Buchungsstapel | [`Klaerungs-Tool.html`](tools/klaerungs-tool.html) |
| **Rechnungsnummern-Prüfung** | Prüft die Rechnungsnummern der Debitoren (Belegfeld 1) auf Fortlaufigkeit. Ergebnis sind zwei Listen: fehlende Nummern und Nummern außerhalb des Schemas. Dazu kommt eine Klärungs-E-Mail an den Mandanten. | nein, nur lesend | [`Rechnungsnummern-Pruefung.html`](tools/rechnungsnummern-pruefung.html) |
| **Differenzbesteuerung-Umbuchung** | Ermittelt je Vorgang die Marge aus Erlös- und Wareneingangsbuchung. Die Umbuchung auf das umsatzsteuerpflichtige Erlöskonto übergibt es als Buchungsstapel. | ja, als Buchungsstapel | [`Differenzbesteuerung-Umbuchung.html`](tools/differenzbesteuerung-umbuchung.html) |

---

## Voraussetzungen

- Windows-Arbeitsplatz mit **DATEV Rechnungswesen**
- **DATEVconnect** (On-Premises) mit der Schnittstelle *Accounting*, installiert und lizenziert
- Optional für Mandantenname, Briefanrede und E-Mail-Adresse (Klärungs-Tool,
  Rechnungsnummern-Prüfung): die DATEVconnect-Schnittstelle für die **zentralen Stammdaten**
  (*Client Master Data*). Sie ist gesondert lizenziert. Ohne sie tragen Sie diese Angaben von Hand ein.
- Zusatzlizenz DATEV connect Kontobuchungen, bestellbar im DATEV Shop
- Ein aktueller Browser (Microsoft Edge oder Google Chrome)
- Die Rechte für den jeweiligen Mandantenbestand in der DATEV Benutzer- und Rechteverwaltung.

---

## So benutzen Sie ein Tool

1. Laden Sie die HTML-Datei herunter (Dateiname in der Tabelle oben anklicken, dann *Download raw file*).
2. Speichern Sie die Datei auf dem Rechner, auf dem DATEV läuft.
3. Öffnen Sie die Datei per Doppelklick. Sie startet im Browser.
4. Wählen Sie Mandant und Wirtschaftsjahr und folgen Sie den Schritten im Tool.

Die Anmeldung an DATEVconnect läuft über Ihre Windows-Sitzung. Benutzername oder Passwort
geben Sie im Tool nicht ein.

### DATEVconnect-Adresse anpassen

Die Tools verbinden sich fest mit

```
http://localhost:58454/datev/api
```

Die Adresse lässt sich in der Oberfläche bewusst nicht ändern. Wenn Ihre Kanzlei **HTTPS** nutzt
oder DATEVconnect auf einem anderen Rechner läuft, öffnen Sie die HTML-Datei in einem Texteditor.
Ganz oben im Skript steht dieser Block:

```js
/* KONFIGURATION – nur hier ändern */
var DATEVCONNECT_BASE = 'http://localhost:58454/datev/api';
```

Ändern Sie nur diese eine Zeile, zum Beispiel für HTTPS auf
`'https://localhost:58452/datev/api'`, und speichern Sie die Datei.

---

## Datenschutz und Sicherheit

- **Die Tools laufen vollständig lokal in Ihrem Browser.** Sie senden keine Daten an
  AHA Consulting oder an Dritte.
- Sie verbinden sich **nur mit DATEVconnect** unter der oben genannten Adresse.
- Sie laden **keine externen Skripte, Schriften oder Tracker** nach.
- Sie speichern nichts im Browser: keine Cookies, kein lokaler Speicher. Nach dem Neuladen ist
  alles weg.
- **E-Mails** (Klärungs-Tool, Rechnungsnummern-Prüfung): Das Tool übergibt Empfänger, Betreff und
  Text an Ihr Mailprogramm. Versendet wird erst, wenn **Sie** dort auf *Senden* klicken. Prüfen Sie
  den Text vorher. Sehr lange E-Mails kürzt Outlook ohne Rückmeldung. Nutzen Sie dann die Funktion
  *Kopieren* im Tool.
- Im Kopfbereich jedes Tools steht ein Link auf ein Formular. Er öffnet sich nur, wenn Sie
  daraufklicken, und überträgt dabei keine Daten aus dem Tool.

---

## Wichtige Hinweise

- **Prüfen Sie die Ergebnisse fachlich.** Die Tools unterstützen Ihre Arbeit, sie ersetzen nicht
  Ihre Beurteilung. Das gilt besonders für Zuordnungen, Margen und Buchungsvorschläge.
- **Buchungsstapel** prüfen Sie in DATEV Rechnungswesen, bevor Sie sie weiterverarbeiten oder
  festschreiben.
- Die Tools sind für die **berufliche Nutzung** in der Buchhaltung gedacht.
- Die Tools werden **unentgeltlich** und **so, wie sie sind** bereitgestellt (siehe [LICENSE](LICENSE)).
  Sie nutzen sie in eigener Verantwortung. Eine gesetzlich zwingende Haftung bleibt unberührt.
- Wenn Sie ein Tool verändern, sind Sie für Ihre Fassung selbst verantwortlich.

---

## Kein Support

Die Tools werden **ohne Support** bereitgestellt:

- keine Beantwortung von Fragen zur Einrichtung oder Nutzung, auch nicht per E-Mail,
- keine Anpassungen oder neuen Funktionen auf Anfrage,
- keine Zusage zu Fehlerkorrekturen oder Updates.

---

## Lizenz

[MIT-Lizenz](LICENSE), © 2026 AHA Consulting GmbH

Sie dürfen die Tools nutzen, verändern und weitergeben, auch kommerziell, solange der
Lizenz- und Copyright-Hinweis erhalten bleibt.

---

## Marken

DATEV, DATEV Rechnungswesen und DATEVconnect sind Marken der DATEV eG. Dieses Repository ist
kein Angebot der DATEV eG und steht in keiner Verbindung zu ihr.
