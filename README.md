# Fahrspurerkennung in Videos

## Hintergrund
Dieses Projekt zielt darauf ab, eine grundlegende Fahrspurerkennung für Fahrassistenzsysteme in Python unter Verwendung der OpenCV-Bibliothek zu implementieren. Es demonstriert, wie man mit Bildverarbeitungstechniken Fahrspuren in Videos erkennen kann. Diese Technik ist fundamental für autonome Fahrzeuge und Fahrerassistenzsysteme, um die Fahrspur zu verstehen und zu halten.

## Projektbeschreibung
Das Projekt verwendet eine Kombination aus Bildverarbeitungsmethoden, um Fahrspuren auf der Straße zu erkennen und zu markieren. Es umfasst mehrere Schritte: Kanten Erkennung, Definition eines Interessensbereichs, Linienfindung mit der Hough-Transformation und das Mitteln und Extrapolieren dieser Linien, um klare Darstellungen der Fahrspuren zu erstellen. Die Ergebnisse werden in Echtzeit auf das Videomaterial überlagert, wodurch die erkannten Fahrspuren visuell dargestellt werden.

## Technologien
- **Programmiersprache**: Python 3.x
- **Hauptbibliotheken**: OpenCV für Bildverarbeitung, NumPy für numerische Berechnungen

## Implementierungsdetails
### Kanten Erkennung
Zunächst wandeln wir das Bild in Graustufen um und verwenden dann den Canny-Algorithmus, um Kanten im Bild zu erkennen. Dies hilft, die relevanten Linien (Fahrspuren) vom Rest des Bildes zu unterscheiden.
### Interessensbereich
Um die Verarbeitung zu vereinfachen und die Genauigkeit zu erhöhen, schränken wir die Bildanalyse auf einen Bereich ein, in dem sich Fahrspuren typischerweise befinden. Dies wird durch das Definieren eines polygonalen Bereichs erreicht, der den unteren Teil des Bildes abdeckt.
### Linienfindung mit der Hough-Transformation
Auf das vorverarbeitete Bild wenden wir die Hough-Transformation an, um Linien zu finden. Diese Transformation ist effektiv bei der Erkennung von Linien in Bildern und wird hier verwendet, um potenzielle Fahrspurmarkierungen zu identifizieren.
### Mittelung und Extrapolation von Linien
Da die Hough-Transformation möglicherweise mehrere Fragmente für jede Fahrspur findet, mitteln wir diese Linien und extrapolieren sie, um zwei klare Linien für die linke und rechte Fahrspur zu erhalten.

## Ergebnis
Et voila! :-)
![Alt](https://github.com/ange-nguetsop/Lane_detection_py/blob/master/GifOutput.gif)
