### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET versucht nun, fehlerhafte SQL-Verbindungen automatisch wieder verbunden

|   |   |
|---|---|
|Details|Ab .NET Framework 4.5.1 wird .NET Framework versucht, fehlerhafte SQL-Verbindungen automatisch wiederherzustellen. Obwohl dies in der Regel apps zuverlässiger durchführen, stehen Grenzfälle, in denen eine app muss wissen, dass die Verbindung getrennt wurde, damit es bestimmte Aktionen beim erneuten Herstellen einer Verbindung ausführen kann.|
|Vorschlag|Wenn diese Funktion aus Gründen der Kompatibilität nicht erwünscht ist, können sie durch Festlegen von deaktiviert die <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> Eigenschaft einer Verbindungszeichenfolge (oder <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) auf 0.|
|Bereich|Edge|
|Version|4.5.1|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

