### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>Es wird versucht, eine TCP/IP-Verbindung mit einer SQL Server-Datenbank, die aufgelöst wird `localhost` ein Fehler auftritt

|   |   |
|---|---|
|Details|In .NET Framework 4.6 und 4.6.1 versucht, eine TCP/IP-Verbindung mit einer SQL Server-Datenbank, die aufgelöst wird <code>localhost</code> tritt der Fehler &quot;netzwerkbezogener oder Instanzspezifischer Fehler beim Herstellen einer Verbindung mit SQL Server. Der Server wurde nicht gefunden oder es konnte nicht auf ihn zugegriffen werden. Stellen Sie sicher, dass der Instanzname richtig und SQL Server so konfiguriert ist, das Remoteverbindungen zulässig sind. (Anbieter: SQL Network Interfaces, Fehler: 26 - Fehler beim Suchen von Server-Instanz angegeben.)&quot;|
|Vorschlag|Dieses Problem wurde behoben wurde, und das vorherige Verhalten in .NET Framework 4.6.2 wiederhergestellt. Verbindung mit einer SQL Server-Editions, die aufgelöst wird <code>localhost</code>, ein Upgrade auf .NET Framework 4.6.2.|
|Bereich|Gering|
|Version|4.6|
|Typ|Laufzeit|

