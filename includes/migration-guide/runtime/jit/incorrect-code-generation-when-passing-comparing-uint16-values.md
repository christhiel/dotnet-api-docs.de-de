### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>Falsche codegenerierung beim übergeben und Vergleichen von UInt16-Werten

|   |   |
|---|---|
|Details|Aufgrund von Änderungen, die in der .NET Framework-4.7 eingeführt wurden, in einigen Fällen vom JIT-Compiler in Anwendungen auf die .NET Framework-4.7 falsch generierte Code vergleicht zwei <code>T:System.UInt16</code> Werte. Weitere Informationen finden Sie unter [Problem #11508: lautlose beim übergeben und Vergleichen von "ushort" Args](https://github.com/dotnet/coreclr/issues/11508) auf "github.com".|
|Vorschlag|Wenn Sie Probleme beim Vergleich von 16-Bit, die in der .NET Framework-4.7 Werte ohne Vorzeichen auftreten, aktualisieren Sie auf .NET Framework 4.7.1.|
|Bereich|Edge|
|Version|4.7|
|Typ|Laufzeit|

