### <a name="only-tls-10-11-and-12-protocols-supported-in-systemnetservicepointmanager-and-systemnetsecuritysslstream"></a>Nur Tls 1.0, 1.1 und 1.2-Protokolle, die nur in System.Net.ServicePointManager und System.Net.Security.SslStream unterstützt

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.6 der <xref:System.Net.ServicePointManager> und <xref:System.Net.Security.SslStream> dürfen die Klassen nur eine der drei folgenden Protokolle verwenden: TLS1. 0, Tls1.1 oder TLS 1.2. Weder das SSL3.0-Protokoll noch das RC4-Verschlüsselungsverfahren werden unterstützt.|
|Vorschlag|Die empfohlene Minderung besteht, die serverseitige app auf TLS1. 0, Tls1.1 oder TLS 1.2 zu aktualisieren. Wenn dies nicht möglich ist oder die Client-Apps fehlerhaft sind, kann die Klasse <xref:System.AppContext?displayProperty=name> verwendet werden, um das Feature auf zwei verschiedene Art und Weisen abzuwählen: <ol><li>Programmgesteuert durch Festlegen/Compat Schaltet die <xref:System.AppContext?displayProperty=name>, wie erläutert unter [hier](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>Indem Sie die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> Abschnitt der Datei "App.config": <code>&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSchUseStrongCrypto=true&quot;/&gt;</code>;</li></ol>|
|Bereich|Gering|
|Version|4.6|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Net.SecurityProtocolType.Ssl3?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl2?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl3?displayProperty=nameWithType></li></ul>|

