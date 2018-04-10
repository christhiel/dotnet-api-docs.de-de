### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>Persischen Kalender verwendet jetzt den Hijri-solaralgorithmus

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.6 der <xref:System.Globalization.PersianCalendar?displayProperty=name> Klasse verwendet den Hijri-solaralgorithmus. Konvertieren von Datumsangaben zwischen dem <xref:System.Globalization.PersianCalendar?displayProperty=name> und anderen Kalender erzeugen eine etwas anderes Ergebnis mit .NET Framework 4.6 für Datumsangaben vor 1800 oder später als 2023 (gregorianischen) beginnt. Darüber hinaus <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> ist jetzt <code>March 22, 0622 instead of March 21, 0622</code>.|
|Vorschlag|Beachten Sie, dass einige frühe oder späte Datumsangaben bei der Verwendung des persischen Kalenders in .NET 4.6 möglicherweise etwas anders aussehen. Speichern Sie zudem beim Serialisieren von Daten zwischen Prozessen, die möglicherweise unter verschiedenen Versionen von .NET Framework ausgeführt werden, die Daten nicht als PersionCalendar-Datumszeichenfolgen (da diese Werte abweichen können).|
|Bereich|Gering|
|Version|4.6|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

