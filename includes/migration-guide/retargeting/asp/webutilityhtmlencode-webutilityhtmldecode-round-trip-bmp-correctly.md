### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode und WebUtility.HtmlDecode Round-Trip BMP ordnungsgemäß

|   |   |
|---|---|
|Details|Für Anwendungen, die als .NET Framework 4.5, Zeichen, die sich außerhalb der Roundtrip Basic Multilingual Plane (BMP) befinden Ziel, bei der Übergabe an die <xref:System.Net.WebUtility.HtmlDecode(System.String)> Methoden.|
|Vorschlag|Diese Änderung haben keine Auswirkungen auf aktuelle Anwendungen, aber das ursprüngliche Verhalten wiederherzustellen fest der <code>targetFramework</code> Attribut von der <code>&lt;httpRuntime&gt;</code> Element in eine Zeichenfolge als &quot;4.5&quot;. Sie können die <code>unicodeEncodingConformance</code>- und <code>unicodeDecodingConformance</code>-Attribute des <code>&lt;webUtility&gt;</code>-Konfigurationselements auch festlegen, um dieses Verhalten unabhängig von der Zielversion von .NET Framework zu steuern.|
|Bereich|Edge|
|Version|4.5|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

