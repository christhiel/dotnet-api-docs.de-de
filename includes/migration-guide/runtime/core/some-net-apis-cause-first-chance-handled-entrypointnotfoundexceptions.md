### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>Einige .NET APIs Ursache erste-Chance EntryPointNotFoundExceptions (behandelt)

|   |   |
|---|---|
|Details|In .NET Framework 4.5, eine kleine Anzahl von .NET Methoden begann auslösen erste Chance <xref:System.EntryPointNotFoundException?displayProperty=name>s. Diese Ausnahmen wurden in .NET Framework behandelt, konnten aber die Testautomatisierung unterbrechen, die keine erstmaligen Ausnahmen erwartete. Dieselben APIs stören einige ApiVerifier-Szenarien, wenn „HighVersionLie“ aktiviert ist.|
|Vorschlag|Dieser Fehler kann durch ein Upgrade auf .NET Framework 4.5.1 vermieden werden. Alternativ können Sie für die Automatisierung aktualisiert werden kann, um nicht bei der ersten Chance unterbrochen <xref:System.EntryPointNotFoundException?displayProperty=name>s.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

