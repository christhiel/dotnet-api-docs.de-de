### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>Verursacht einen SqlConnection.Open unter Windows 7 mit nicht - IFS-Winsock BSP oder LSP vorhanden

|   |   |
|---|---|
|Details|<xref:System.Data.SqlClient.SqlConnection.Open> und <xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)> in .NET Framework 4.5 schlägt fehl, wenn auf dem Computer vorhanden, die auf einem Windows 7-Computer mit einem nicht - IFS-Winsock BSP oder LSP ausgeführt sind. Bestimmt, ob ein nicht - IFS BSP oder LSP installiert wurde, verwenden die <code>netsh WinSock Show Catalog</code> Befehl, und untersuchen Sie jeder <code>Winsock Catalog Provider Entry</code> Element, das zurückgegeben wird. Wenn für den Servicekennzeichenwert das <code>0x20000</code>-Bit gesetzt ist, verwendet der Anbieter IFS-Handle und funktioniert daher ordnungsgemäß. Wenn das <code>0x20000</code>-Bit leer (nicht festgelegt) ist, handelt es sich um ein Nicht-IFS-BSP oder -LSP.|
|Vorschlag|Dieses Problem wurde in .NET Framework 4.5.2 behoben, daher kann es durch ein Upgrade von .NET Framework vermieden werden. Alternativ kann es durch Entfernen aller installierten Nicht-IFS-Winsock-LSPs vermieden werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

