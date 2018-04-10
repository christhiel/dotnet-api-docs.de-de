### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a>Bidirektionale Datenbindung an eine Eigenschaft mit einem nicht öffentlichen Setter wird nicht unterstützt.

|   |   |
|---|---|
|Details|Der Versuch, Daten ohne einen öffentlichen Setter an eine Eigenschaft zu binden, wurde nie unterstützt. Ab .NET Framework 4.5.1 ist dieses Szenario löst ein <xref:System.InvalidOperationException?displayProperty=name>. Beachten Sie, dass diese neue Ausnahme nur für Apps ausgelöst wird, die speziell auf .NET Framework 4.5.1 abzielen. Wenn eine App auf .NET Framework 4.5 ausgerichtet ist, wird der Aufruf zugelassen. Wenn die App nicht auf eine bestimmte Version von .NET Framework ausgerichtet ist, wird die Bindung als unidirektionale Bindung behandelt.|
|Vorschlag|Die App sollte aktualisiert werden, um entweder die unidirektionale Bindung zu verwenden oder den Setter der Eigenschaft öffentlich zur Verfügung zu stellen. Alternativ können Sie die App auf .NET Framework 4.5 ausrichten, um das alte Verhalten zu erreichen.|
|Bereich|Gering|
|Version|4.5.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|

