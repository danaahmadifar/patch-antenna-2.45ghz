# Inset-Fed Patch Antenne (2.45 GHz) - BHT Labor

In diesem Repository liegen der Laborbericht, die Simulationsdateien und die Messergebnisse zu unserem Projekt im Modul *Antennen und Wellenausbreitung* an der Berliner Hochschule für Technik (BHT, Sommersemester 2024).

Ziel war es, eine Inset-Fed Patch-Antenne für 2,45 GHz zu berechnen, zu simulieren, auf einer FR4-Platine zu fräsen und anschließend im Labor auszumessen.

---

## Wichtigste Daten

* **Resonanzfrequenz:** 2,45 GHz
* **Material:** FR4-Epoxy (Dicke = 1,6 mm, $\epsilon_r = 4,4$)
* **Patch-Größe:** Breite $W = 37,23	ext{ mm}$, Länge $L = 28,81	ext{ mm}$
* **Einschnitt (Inset):** Tiefe $d = 10,59	ext{ mm}$, Spaltbreite $s = 0,5	ext{ mm}$
* **Zuleitung:** 50-Ohm-Mikrostreifenleitung (Breite = 3,06 mm)

---

## Ablauf

1. **Berechnung:** Maße und Inset-Tiefe mit Formeln für Rechteck-Patchantennen ausgerechnet.
2. **Simulation:**
   * **Ansys HFSS:** Für das 3D-Modell, E-Felder und das Abstrahlverhalten.
   * **Keysight ADS:** Zum Gegenchecken und Exportieren der Gerber-Dateien für die Fräsmaschine.
3. **Fertigung & Messung:**
   * Platine gefräst und SMA-Buchse angelötet.
   * Zusätzlich einen einfachen Lambdaviertel-Dipol gebaut, um Werte zu vergleichen.
   * Gemessen mit NanoVNA ($S_{11}$), Spektrumanalysator und Signalgenerator (Nah- und Fernfeld, Polarisation).

---

## Kurzfassung der Ergebnisse

* **Anpassung ($S_{11}$):** Das beste Minimum lag bei 2,471 GHz. Bei der Ziel-Frequenz von 2,45 GHz lag $S_{11}$ bei etwa -16 dB, was gut funktioniert hat. Die kleine Verschiebung kommt wahrscheinlich vom Lötzinn und Toleranzen beim Fräsen/Material.
* **Gewinn:** Gemessen haben wir ca. 2 dBi in Hauptstrahlrichtung.
* **Polarisation:** Bei 90° Drehung der Empfangsantenne ist das Signal um etwa 20 dB eingebrochen. Die lineare Polarisation passt also.

---

## Ordnerstruktur

* `docs/` - Der vollständige Laborbericht als PDF
* `cad/` - Gerber-Dateien zum Fräsen (Top, Bottom, Outline)
* `images/` - Fotos von den fertigen Platinen und den Messungen

---

## Gruppe

* Dana Ahmadifar
* Niklas Walther
* Mehran Akbarzadeh
* Armin Nikdel Amand

**Betreuung:** Prof. Dr.-Ing. Jörg Braune (BHT)
