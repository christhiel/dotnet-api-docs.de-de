### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>Eine NullReferenceException, HttpRuntime.AppDomainAppPath

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2, löst die Laufzeit eine <code>T:System.NullReferenceException</code> beim Abrufen einer <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> -Wert, der Null-Zeichen enthält. In .NET Framework 4.6.1 und früheren Versionen, löst die Laufzeit eine <code>T:System.ArgumentNullException</code>.|
|Vorschlag|Sie können die gehen Sie folgendermaßen vor, um zu dieser Änderung reagieren Möglichkeiten:<ul><li>Behandeln der <code>T:System.NullReferenceException</code> Wenn Ihre Anwendung auf .NET Framework 4.6.2 ausgeführt werden.</li><li>Upgrade auf die .NET Framework-4.7, wird das vorherige Verhalten wiederhergestellt und löst eine <code>T:System.ArgumentNullException</code>.</li></ul>|
|Bereich|Edge|
|Version|4.6.2|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

