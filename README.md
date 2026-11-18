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