### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>Erstellen einer Edmx Entity Framework mit Visual Studio 2013 kann mit Fehler MSB4062 fehlschlagen, wenn die EntityDeploySplit oder EntityClean mit

|   |   |
|---|---|
|Details|MSBuild 12.0-Tools (enthalten in Visual Studio 2013) geändert, MSBuild-Dateispeicherorte, ungültig werden ältere Entity Framework-Targets-Dateien verursacht wird. Das führt dazu, dass <code>EntityDeploySplit</code>- und <code>EntityClean</code>-Aufgaben fehlschlagen, da sie <code>Microsoft.Data.Entity.Build.Tasks.dll</code> nicht finden können. Beachten Sie, dass diese Unterbrechung nicht aufgrund einer Änderung Toolset (MSBuild/VS) aufgrund einer Änderung der .NET Framework ist. Es tritt nur beim Upgrade von Entwicklertools und nicht beim Aktualisieren von .NET Framework auf.|
|Vorschlag|Entity Framework Targets-Dateien werden so repariert, arbeiten mit dem neuen MSBuild Layout Anfang in .NET Framework 4.6. Ein Upgrade auf diese Version von .NET Framework wird dieses Problem beheben. Alternativ können Sie [diese](http://stackoverflow.com/a/24249247/131944) Problemumgehung verwenden, um die Zieldateien direkt zu patchen.|
|Bereich|Hauptversion|
|Version|4.5.1|
|Typ|Neuzuweisung|

