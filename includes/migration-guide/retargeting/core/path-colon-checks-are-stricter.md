### <a name="path-colon-checks-are-stricter"></a>Doppelpunkt pfadprüfungen sind strenger

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2 wurden eine Reihe von Änderungen vorgenommen, um zuvor nicht unterstützte Pfade (sowohl in der Länge und Format) zu unterstützen. Prüft auf richtige Laufwerk Trennzeichen (Doppelpunkt)-Syntax mehr korrekt ist, wurden die hatte den Nebeneffekt einige URI Pfade in ein paar select Pfad-APIs, in denen sie verwendet, um toleriert werden, werden, blockiert.|
|Vorschlag|Wenn einen URI an die betroffenen APIs übergeben werden soll, ändern Sie die Zeichenfolge, um zuerst einen gültigen Pfad sein.<ul><li>Entfernen Sie das Schema manuell aus den URLs (z. B. entfernen <code>file://</code> aus URLs)</li><li>Übergeben Sie den URI der <xref:System.Uri> Klasse, und verwenden <xref:System.Uri.LocalPath></li></ul>Alternativ können Sie den neuen Pfad Normalisierung abwählen, durch Festlegen der <code>Switch.System.IO.UseLegacyPathHandling</code> AppContext Switch auf "true".|
|Bereich|Edge|
|Version|4.6.2|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

