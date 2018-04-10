### <a name="entity-framework-version-must-match-the-net-framework-version"></a>Entity Framework-Version muss der .NET Framework-Version entsprechen.

|   |   |
|---|---|
|Details|Die Entity Framework-Version sollte mit der .NET Framework-Version übereinstimmen. Entity Framework 5 wird für .NET 4.5 empfohlen. Es gibt einige bekannte Probleme mit EF 4.x in einem Projekt auf .NET 4.5 um <xref:System.ComponentModel.DataAnnotations>. In .NET 4.5 wurden diese in einer anderen Assembly verschoben, daher gibt es Probleme bestimmen die Anmerkungen zu verwenden.|
|Vorschlag|Upgrade auf Entity Framework 5 für .NET Framework 4.5|
|Bereich|Hauptversion|
|Version|4.5|
|Typ|Neuzuweisung|

