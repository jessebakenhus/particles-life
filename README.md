# Particles Life

Ein Uni-Projekt, das zeigt, wie in einem zweidimensionalen Raum aus einfachen Regeln komplexe Muster entstehen (Emergenz). Nebenbei üben wir dabei den Teamworkflow.

## So funktioniert die Logik

Partikeltypen ziehen sich gegenseitig an oder stoßen sich ab, jeweils unterschiedlich stark. Aus wenigen lokalen Regeln entstehen so Muster, die wir nicht direkt programmiert haben.

Die **Interaktionsmatrix** bestimmt maßgeblich, wie sich die Partikel verhalten. Ein Beispiel:

| Typ | A     | B     | C     | D     |
|-----|-------|-------|-------|-------|
| **A** | +0.5  | -0.3  | +0.8  | 0.0   |
| **B** | -0.7  | +0.2  | 0.0   | +0.4  |
| **C** | +0.1  | +0.6  | -0.4  | -0.2  |
| **D** | 0.0   | -0.5  | +0.7  | +0.3  |

Zusätzlich spielen der Abstand zwischen den Partikeln und globale Simulationsparameter eine Rolle.

## Betriebssystem

- **Ubuntu:** Python 3.12, 3.13 oder 3.14
- **Windows:** eine unterstützte Python-Version
- **macOS:** eine unterstützte Python-Version

## Aufteilung der Pakete 

- 📁`application`: Verbindung der Logik der Partikel und der Oberfläche
  - 🐍 `simulation_service.py`: kümmert sich darum um die Simulation zu starten, anpassen und stoppen
- 📁`domain`: 
  - 🐍 `model.py`: einzelne Objekt-Modell die wir benötigen
  - 🐍 `simulation.py`: Gesamte Mathematik bzw. Physik hinter der Simulation und die Simulation ansich. 
- 📁`viz`: Alles rund um die Oberfläche
  - 🐍 `ui.py`: nur die reine Oberfläche. Diese Datei soll kein Wissen über die Logik haben. Soll nur der Anzeige dienen.
  - 🐍 `viewmodel.py`: verbindet die Oberfläche (siehe `ui`) mit der konkreten Logik, die aus dem Application-Layer `application` kommt.
- 🐍 `app.py`: von hier startet alles. Der zentrale Entry-Point.

