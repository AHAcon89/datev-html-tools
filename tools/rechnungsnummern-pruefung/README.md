# Rechnungsnummern-Prüfung

Prüft die Rechnungsnummern der Debitoren auf Fortlaufigkeit.

**Datei:** [`rechnungsnummern-pruefung.html`](rechnungsnummern-pruefung.html) – Datei anklicken, dann *Download raw file*.
**Aktuelle Version:** 1.2.2
**Schreibt in DATEV:** nein, nur lesend

## Was das Tool macht
- Ermittelt die Debitorenkonten des Mandanten und liest deren Buchungen.
- Wertet die Rechnungsnummern in Belegfeld 1 aus. Sie legen fest, ab welcher Stelle der Zähler
  beginnt (Vorgabe: Stelle 3); die Zeichen davor gelten als Präfix.
- Jedes Präfix bildet eine eigene Nummernfolge und lässt sich einzeln abwählen.
- Ergebnis sind zwei Listen: **fehlende Rechnungsnummern** und **Nummern außerhalb des Schemas**.
- Erstellt auf Wunsch eine Klärungs-E-Mail an den Mandanten.

## Grenzen
- Nummern am Anfang und Ende einer Folge sind nicht prüfbar (sie können im Vor- oder Folgejahr liegen).
- Eine Folge mit nur einer Nummer gilt als nicht prüfbar.
- Eine nie gebuchte Rechnung am Ende der Folge hinterlässt keine Lücke.
- Lange E-Mails kürzt Outlook ohne Rückmeldung. Ab etwa sieben Lücken nutzen Sie *Kopieren*.

Voraussetzungen, Datenschutz und Nutzungsbedingungen: siehe [README im Hauptverzeichnis](../../README.md).
