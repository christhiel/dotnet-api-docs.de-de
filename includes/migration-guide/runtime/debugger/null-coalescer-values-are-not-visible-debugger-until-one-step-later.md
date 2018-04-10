### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Zusammenfügungsfunktion NULL-Werte sind bis zu einem späteren Zeitpunkt ein Schritt nicht sichtbar ist, im debugger

|   |   |
|---|---|
|Details|Ein Fehler in .NET Framework 4.5 bewirkt, dass Werte, die über eine null zusammenfügende Operation festgelegt wird, werden nicht in den Debugger sichtbar, sofort nach der Zuweisungsvorgang ausgeführt wird, wenn auf die 64-Bit-Version des Frameworks ausgeführt wird.|
|Vorschlag|Eine zusätzliche Zeit im Debugger schrittweise führt dazu, dass der lokale/Wert des Felds korrekt aktualisiert werden. Darüber hinaus wurde in .NET Framework 4.6 dieses Problem behoben; Upgrade auf diese Version des Frameworks, sollte das Problem beheben.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|

