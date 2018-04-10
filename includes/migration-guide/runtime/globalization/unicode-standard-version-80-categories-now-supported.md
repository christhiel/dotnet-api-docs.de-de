### <a name="unicode-standard-version-80-categories-now-supported"></a>Unicode-standard-Version 8.0 Kategorien jetzt unterstützt.

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2 wurde Unicode-Daten im Rahmen von Unicode-standard-Version 6.3 auf Version 8.0 aktualisiert.  Klicken Sie zum Anfordern von Unicode-Zeichen-Kategorie in .NET Framework 4.6.2 entsprechen einige Ergebnisse möglicherweise nicht die Ergebnisse in früheren Versionen von .NET Framework.  So ändern Sie größtenteils wirkt sich Cherokee Unterschiede zwischen auf und neue Protoko des Eintrags Vokale signiert und Betonungszeichen.|
|Vorschlag|Überprüfen Sie Code, und klicken Sie mit der entfernen/ändern Logik, von denen hartcodierte Unicode-Zeichenkategorien abhängt.|
|Bereich|Gering|
|Version|4.6.2|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

