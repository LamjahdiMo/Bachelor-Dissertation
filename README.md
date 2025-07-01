# Dynamische Regelung der Walzkraft beim mechanischen Festwalzen
[![DOI](https://zenodo.org/badge/1012079348.svg)](https://doi.org/10.5281/zenodo.15786688)


## Über die Arbeit

Diese Bachelorarbeit behandelt die Entwicklung, Simulation und Implementierung eines Regelungssystems zur dynamischen Steuerung der Walzkraft beim mechanischen Festwalzen. Im Fokus steht der Umgang mit Transferstagnation und Störeinflüssen im Walzprozess unter Verwendung moderner regelungstechnischer Ansätze wie PID-Regler, Smith-Prädiktor und innovativen Schätzverfahren.

## Ziel der Arbeit

Ziel ist es, ein intelligentes Regelkonzept zu entwickeln, das:

- die durch Kommunikationsverzögerungen verursachte Transferstagnation kompensiert,
- externe Störungen herausfiltert,
- die Festwalzkraft positionsabhängig und in Echtzeit regelt,
- auf einem Industrie-PC (IPC) mit TwinCAT umgesetzt werden kann.

## Methodik

Die Arbeit gliedert sich in mehrere Phasen:

1. **Theoretische Grundlagen & Literaturrecherche**
   - Regelungstechnik, LTI-Systeme, Laplace-Transformation, PID-, I-, D-Regler
   - Bode-Diagramm, Stabilitätskriterien (Nyquist, Hurwitz)

2. **Analyse des Walzprozesses**
   - Charakterisierung des Festwalzverhaltens
   - Problematische Einflüsse wie Totzeiten und Störungen

3. **Regelungsansätze**
   - PID-Regler mit und ohne Modifikation
   - Smith-Schätzer zur Kompensation von Totzeiten
   - Zwei eigens entwickelte Schätzer (M.A.- und M.E.-Schätzer)

4. **Simulation & Verifikation**
   - MATLAB/Simulink, SolidWorks, Ansys
   - TwinCAT-Programmierung, Beckhoff-Dashboard
   - Testen unter realitätsnahen, auch extremen Bedingungen

## Ergebnisse

- Die Kombination aus Echtzeit-Mittelwert-Schätzung, Smith-Vorsteuerung und optimierten PID-Parametern liefert die stabilste und effizienteste Regelung.
- Die entwickelten Schätzer verbesserten die Reaktionsfähigkeit signifikant.
- Die entwickelte Lösung ist robust gegenüber Störungen und für industrielle Anwendungen geeignet.

## Technologien & Tools

- **Simulink / MATLAB**
- **Beckhoff TwinCAT / Windows-Control**
- **Python (für Analyse & Datenverarbeitung)**
- **SolidWorks, Ansys**
- **OPC-UA** zur Kommunikation zwischen Steuerung und Sensorik

## Betreuer & Prüfende

- **Institut:** Institut für Fertigungstechnik und Werkzeugmaschinen (IFW)
- **Erstprüfer:** Prof. Dr.-Ing. Bernd Ponick
- **Zweitprüfer:** (nicht spezifiziert)

## Abgabe

- **Datum:** September 2024
- **Ort:** Garbsen / Universität Hannover

## Hinweis

Diese Arbeit wurde eigenständig angefertigt. Jegliche Hilfe ist im Literaturverzeichnis kenntlich gemacht. Der Quellcode und die ausführbaren Implementierungen befinden sich nicht im Repository dieser Datei und sind ggf. beim Autor auf Anfrage erhältlich.

---

