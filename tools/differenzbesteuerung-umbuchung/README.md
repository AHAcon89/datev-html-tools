# Differenzbesteuerung-Umbuchung

Ermittelt die Marge je Vorgang für die Differenzbesteuerung und bucht sie auf das
umsatzsteuerpflichtige Erlöskonto um.

**Datei:** [`differenzbesteuerung-umbuchung.html`](differenzbesteuerung-umbuchung.html) – Datei anklicken, dann *Download raw file*.
**Aktuelle Version:** 1.2.2
**Schreibt in DATEV:** ja, als Buchungsstapel (nicht festgeschrieben)

## Was das Tool macht
- Ordnet Erlös- und Wareneingangsbuchungen einander zu, über den Buchungstext oder eine
  Zusatzinformation. Verglichen wird der gesamte Feldinhalt, ohne Groß-/Kleinschreibung und Sonderzeichen.
- Sucht den Wareneingang bei Bedarf auch in älteren Wirtschaftsjahren.
- Marge je Vorgang = Erlös minus Wareneingang.
- Schlägt die Konten nach Kontenrahmen vor (Erlös differenzbesteuert / Umbuchungskonto / Wareneingang):
  SKR 04: 4134 / 4132 / 5238 · SKR 03: 8197 / 8199 / 3293 · SKR 51: 8110 / 8111 / 3110.
  Bei anderen Kontenrahmen schlägt es nichts vor.
- Übergibt die Umbuchungen als Buchungsstapel, je Buchungsmonat ein Stapel
  (Bezeichnung „Diffbest. Umbuchung MM/JJ").

## Bitte beachten
- Eine **negative Marge** wird nicht gebucht, nur gemeldet.
- Die Buchung enthält keinen Steuerschlüssel; die Umsatzsteuer ergibt sich aus dem Umbuchungskonto
  (Automatikkonto). Prüfen Sie nach der Übernahme in DATEV, ob die Umsatzsteuer wie erwartet ermittelt wird.
- Vorgänge mit mehreren Buchungen je Seite oder uneinheitlichem Belegfeld 1 markiert das Tool gelb und
  wählt sie nicht vor.

Voraussetzungen, Datenschutz und Nutzungsbedingungen: siehe [README im Hauptverzeichnis](../../README.md).
