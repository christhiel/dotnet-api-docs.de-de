### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase ist nicht mehr von UseRandomizedStringHashAlgorithm zufällig.

|   |   |
|---|---|
|Details|Vor .NET Framework 4.6, den Wert des <xref:System.AppDomainSetup.DynamicBase> würde zufällige werden, zwischen Anwendungsdomänen oder Prozessen, wenn UseRandomizedStringHashAlgorithm in der app-Datei "App.config" aktiviert wurde. Ab .NET Framework 4.6 <xref:System.AppDomainSetup.DynamicBase> stabil Ergebnis zurückgegeben wird, zwischen verschiedenen Instanzen von einer app ausgeführt werden und zwischen verschiedenen app-Domänen. Dynamische Basen werden weiterhin für andere apps unterschiedlich sein. Diese Änderung wird nur die Benennung zufallselement für verschiedene Instanzen der gleichen app entfernt.|
|Vorschlag|Beachten Sie diese aktivieren <code>UseRandomizedStringHashAlgorithm</code> führt nicht zu <xref:System.AppDomainSetup.DynamicBase> wird zufällig. Wenn eine zufällige Basis erforderlich ist, muss es in Ihrer app-Code nicht über diese API erstellt werden.|
|Bereich|Edge|
|Version|4.6|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

