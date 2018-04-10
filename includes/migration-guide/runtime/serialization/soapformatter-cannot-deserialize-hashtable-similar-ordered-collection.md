### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter Hashtabelle kann nicht deserialisiert werden und ähnliche geordnete von Auflistungsobjekten

|   |   |
|---|---|
|Details|Die <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> keine Garantie dafür, dass Objekte unter einer Version von .NET Framework serialisierte unter einer anderen Version erfolgreich deserialisiert wird. Insbesondere sortiert einige Sammlungen (z. B. <xref:System.Collections.Hashtable?displayProperty=name>) Elemente zwischen 4.0 und 4.5 hinzugefügt, sodass Objekte dieser Typen nicht mit .NET 4.0 deserialisiert werden können, wenn sie mit .NET 4.5 serialisiert wurden. Beachten Sie, dass kein Problem auftritt, wenn die serialisierten Daten mit derselben Version von .NET Framework sowohl serialisiert als auch deserialisiert werden.|
|Vorschlag|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> Serialisierung mit ersetzt werden sollte <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> Serialisierung oder <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> flexibel auf .NET Framework geändert werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

