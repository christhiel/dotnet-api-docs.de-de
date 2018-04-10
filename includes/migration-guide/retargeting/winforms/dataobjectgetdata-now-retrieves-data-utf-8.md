### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>DataObject.GetData Ruft Daten jetzt als UTF-8 ab

|   |   |
|---|---|
|Details|Für apps, die auf .NET Framework 4 oder die auf .NET Framework 4.5.1 oder älteren Versionen ausgeführt <code>DataObject.GetData</code> Ruft die HTML-formatierte Daten als ASCII-Zeichenfolge ab. Daher werden nur ASCII-Zeichen (Zeichen mit ASCII-Codes größer als 0x7F) durch zwei zufällige Zeichen dargestellt. Für apps, .NET Framework 4.5 oder höher, und führen auf .NET Framework 4.5.2 ausgerichtet <code>DataObject.GetData</code> ruft von HTML-formatierte Daten als UTF-8, mit dem stellt Zeichen größer als 0x7F korrekt dar.|
|Vorschlag|Wenn Sie eine problemumgehung für das Codierungsproblem mit HTML-formatierten Zeichenfolgen implementiert (z. B. aus der Zwischenablage durch explizites Codieren der HTML-Zeichenfolge durch Übergabe an abgerufen <xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) und das Ziel Ihrer app von Version 4, 4.5, Dieses Problem zu umgehen, sollten entfernt werden. Wenn aus irgendeinem Grund das alte Verhalten erforderlich ist, kann die app .NET Framework 4.0, um dieses Verhalten abzurufen abzielen.|
|Bereich|Edge|
|Version|4.5.2|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

