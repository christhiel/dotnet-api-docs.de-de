### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection kann nicht mehr auf SQL Server 1997 und Datenbanken, die mithilfe des VIA-Adapters eine Verbindung herstellen.

|   |   |
|---|---|
|Details|Verbindungen zu SQL Server-Datenbanken, die über die [Virtual Interface Adapter (VIA)-Protokoll](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) werden nicht mehr unterstützt. Das Protokoll zur Verbindung mit einer SQL Server-Datenbank wird in der Verbindungszeichenfolge angezeigt. Eine Verbindung VIA über enthält:&lt;Servername&gt;. Wenn diese app SQL über ein anderes Protokoll als VIA eine Verbindung herstellt (Tcp: oder Np: z. B.), dann keine unterbrechende Änderung auftreten werden. Darüber hinaus werden Verbindungen mit SQL Server 7 (1997) nicht mehr unterstützt.|
|Vorschlag|Das VIA-Protokoll ist veraltet, sodass ein Protokoll für die Verbindung mit SQL-Datenbanken verwendet werden soll. TCP/IP ist das das am häufigsten verwendete Protokoll vorgibt. Anweisungen zum Aktivieren des TCP/IP-Protokolls verwendbaren [hier](https://msdn.microsoft.com/library/bb909712.aspx). Wenn die Datenbank nur innerhalb eines Intranets aus zugegriffen wird, kann das freigegebene Pipes-Protokoll eine bessere Leistung erzielt, wenn das Netzwerk langsam ist.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

