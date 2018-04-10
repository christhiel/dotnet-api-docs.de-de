### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>Mit der ObjectContext.CreateDatabase-Methode erstellte Protokolldateiname wurde geändert, um SQL Server-Spezifikationen entsprechen.

|   |   |
|---|---|
|Details|Wenn die <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> Methode wird aufgerufen, entweder direkt oder Code First mit dem SqlClient-Anbieter und einen AttachDBFilename-Wert in der Verbindungszeichenfolge verwenden, erstellt es eine Protokolldatei mit dem Namen filename_log.ldf statt Dateiname.ldf (wobei Dateiname ist der Name des die Datei durch den Wert von AttachDBFilename angegeben). Diese Änderung verbessert das Debuggen, indem eine Protokolldatei bereitgestellt wird, die nach den SQL Server-Spezifikationen benannt wird.|
|Vorschlag|Wenn der Name der Protokolldatei für eine App wichtig ist, sollte die App aktualisiert werden, um das standardmäßige Dateinamenformat „_log.ldf“ zu erwarten.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

