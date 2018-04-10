### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>"NetDataContractSerializer" schlägt fehl, beim Deserialisieren von einem ConcurrentDictionary serialisiert mit einer anderen Version von .NET

|   |   |
|---|---|
|Details|Programmbedingt die <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> können verwendet werden, nur, wenn sowohl die Serialisierung und Deserialisierung den gleichen CLR-Typ aufweisen. Aus diesem Grund wird nicht garantiert, dass ein Objekt mit einer Version von .NET Framework serialisiert, die von einer anderen Version deserialisiert werden kann.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> ist ein Typ, der ist bekannt, nicht korrekt deserialisiert werden, wenn mit .NET Framework 4.5 oder einer früheren Version serialisiert und mit .NET Framework 4.5.1 deserialisiert oder höher.|
|Vorschlag|Es gibt eine Anzahl von möglichen problemumgehungen für dieses Problem:<ul><li>Aktualisieren Sie den serialisieren Computer um .NET Framework 4.5.1, ebenfalls zu verwenden.</li><li>Verwendung <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> anstelle von <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> wie dies genauen gleichen CLR-Typen auf Serialisierung und Deserialisierung keine erwartet.</li><li>Verwendung <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> anstelle von <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> , da es nicht diesen bestimmten 4.5 - aufweist&gt;4.5.1 zu unterbrechen.</li></ul>|
|Bereich|Gering|
|Version|4.5.1|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

