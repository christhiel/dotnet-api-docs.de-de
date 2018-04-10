### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>Einem ConcurrentDictionary serialisiert in .NET 4.5 mit "NetDataContractSerializer" kann nicht deserialisiert werden, indem .NET 4.5.1 oder 4.5.2

|   |   |
|---|---|
|Details|Aufgrund interner Änderungen in den Typ <xref:System.Collections.Concurrent.ConcurrentDictionary%602> Objekte, die mit .NET Framework 4.5 serialisiert werden mithilfe der <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> kann nicht deserialisiert werden, in .NET Framework 4.5.1 oder in der .NET Framework-4.5.2.Note in die andere Richtung (d. verschieben Serialisieren mit .NET Framework 4.5.x und die Deserialisierung von mit .NET Framework 4.5) funktioniert. Auf ähnliche Weise alle 4.x versionsübergreifende Serialisierung funktioniert mit der .NET Framework-4.6.Serializing und Deserialisierung mit einer einzigen Version von .NET Framework ist nicht betroffen.|
|Vorschlag|Wenn es zum Serialisieren und Deserialisieren erforderlich ist eine <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> zwischen den .NET Framework 4.5 und .NET Framework-4.5.1/4.5.2, ein alternativer Serialisierer wie die <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> oder <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> Serialisierungsprogramm sollte verwendet werden, statt die <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. Alternativ, da dieses Problem in .NET Framework 4.6 behandelt wird, kann es gelöst werden durch ein Upgrade auf diese Version von .NET Framework.|
|Bereich|Gering|
|Version|4.5.1|
|Typ|Laufzeit|

