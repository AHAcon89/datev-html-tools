# Klärungs-Tool

Gleicht ein Klärungskonto mit den offenen Posten der Kreditoren ab und räumt es über einen
Buchungsstapel auf.

**Datei:** [`klaerungs-tool.html`](klaerungs-tool.html) – Datei anklicken, dann *Download raw file*.
**Aktuelle Version:** 1.4.3
**Schreibt in DATEV:** ja, als Buchungsstapel

## Was das Tool macht
- Liest die Buchungen des Klärungskontos und die offenen Posten der Kreditoren.
- Blendet Buchungen aus, die sich über Belegfeld 1 auf 0,00 € ausgleichen.
- Ordnet die übrigen Buchungen über den Betrag offenen Posten zu (Vergleich mit dem offenen Saldo
  des Postens, umstellbar auf den Ursprungsbetrag, mit einstellbarer Toleranz).
- Markierte Buchungen übergibt es als Storno und Neubuchung in einem Buchungsstapel
  (Bezeichnung „Korr. nachger. Belege MM/JJ").
- Für die nicht markierten Buchungen erstellt es eine Beleganforderung per E-Mail an den Mandanten.
- Eine Expertenansicht zeigt, warum eine Buchung keinem offenen Posten zugeordnet wurde.

## Bitte beachten
- Prüfen Sie Storno und Neubuchung im Buchungsstapel, bevor Sie ihn weiterverarbeiten.
- Prüfen Sie den E-Mail-Text vor dem Senden. Bei langen Listen nutzen Sie *Kopieren* statt
  *Mailprogramm öffnen*.

Voraussetzungen, Datenschutz und Nutzungsbedingungen: siehe [README im Hauptverzeichnis](../../README.md).
