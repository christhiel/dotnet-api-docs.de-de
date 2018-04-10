### <a name="xml-schema-validation-is-stricter"></a>XML-Schema-Validierung ist strenger

|   |   |
|---|---|
|Details|In .NET Framework 4.5 ist ein XML-schemavalidierung strikter. Wenn Sie xsd:anyURI verwenden, um einen URI wie ein mailto-Protokoll zu überprüfen, tritt bei der Validierung ein Fehler auf, wenn der URI Leerzeichen enthält. In früheren Versionen von .NET Framework war die Validierung erfolgreich. Die Änderung betrifft nur Anwendungen, die auf .NET Framework 4.5 abzielen.|
|Vorschlag|Wenn großzügiger ist .NET Framework 4.0-Überprüfung erforderlich ist, kann die Überprüfung Anwendung Version 4.0 von .NET Framework abzielen. Bei der neuzuweisungen in .NET 4.5, sollte jedoch codereviews erfolgen, um sicherzustellen, dass die ungültigen URIs (mit Leerzeichen) werden nicht als Attributwerte mit dem AnyURI-Datentyp erwartet.|
|Bereich|Gering|
|Version|4.5|
|Typ|Neuzuweisung|

