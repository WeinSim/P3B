# Physikpraktikum P3B

GitHub-Repository für das FP-I-A-Physikpraktikum im Sommersemester 2025.
Von Yannic Werner und Simon Weinzierl.

Die Bearbeitung des FP-I-A-Physikpraktikums erfolgt bei uns rein digital.
Unsere Abgaben für die Vor- und Nachbereitung der Versuche sind mit LaTeX
getippt und für die Auswertung verwenden wir an einigen Stellen Python.

Zu jedem der fünf Versuche (BAS, FHV, NMR-A, PLP, ROE) gibt es auf der obersten
Ebene einen Ordner, in dem sich die jeweils dazugehörigen Dateien befinden.

Für jeden Versuch verwenden wir Python für zwei verschiedene Zwecke:
1. **Datenauswertung.**
Unsere Datenauswertung erfolgt rein digital. Sowohl die Berechnung der Ergebnisse
als auch die der Unsicherheit werden vom Python Code übernommen.
Für die Berechnung der Unsicherheit verwenden wir (sofern nicht anders angegeben)
die Gauß'sche Fehlerfortpflanzung. Dazu werden von dem Ausdruck für das
Messergebnis automatisch die partiellen Ableitungen nach allen vorkommenden
Größen bestimmt. Mithilfe der jeweiligen Unsicherheiten der Variablen bzw.
Parameter wird dann die Unsicherheit des Ergebnisses berechnet.
Diese Berechnungen passieren in der Datei `Expressions.py`.
In manchen Fällen muss an eine Datenreihe eine Ausgleichsgerade gefittet
werden. Dazu verwenden wir die Library `numpy`, konkret die Funktion
`numpy.polyfit`. Diese Funktion fittet ein Ausgleichspolynom an die gegebenen
Messpunkte und gibt auch die Unsicherheiten in den Parametern zurück
(Steigung und Y-Achsenabschnitt).

2. **Graphische Darstellung der Daten.** In Experimenten, in denen Messreihen
zu der selben Größe unter verschiedenen Parametern aufgenommen werden,
werden diese oft graphisch dargestellt. Dafür eignet sich das Package
`matplotlib` hervorragend.