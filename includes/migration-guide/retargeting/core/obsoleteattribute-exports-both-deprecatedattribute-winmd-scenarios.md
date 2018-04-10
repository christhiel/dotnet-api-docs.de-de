### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute exportiert als ObsoleteAttribute und DeprecatedAttribute in WinMD-Szenarien

|   |   |
|---|---|
|Details|Bei der Erstellung einer Windows-metadatenbibliothek (winmd-Datei), die <xref:System.ObsoleteAttribute?displayProperty=name> Attribut als sowohl exportiert <xref:System.ObsoleteAttribute?displayProperty=name> und [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Vorschlag|Neukompilierung des vorhandenen Quellcodes, die verwendet die <xref:System.ObsoleteAttribute?displayProperty=name> generiert möglicherweise Warnungen beim Verarbeiten des Codes in C + c++ / CX oder JavaScript.We wird nicht empfohlen, sowohl <xref:System.ObsoleteAttribute?displayProperty=name> und [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) für Code in verwalteten Assemblys aus; sie kann zu Buildwarnungen führen.|
|Bereich|Edge|
|Version|4.5.1|
|Typ|Neuzuweisung|

