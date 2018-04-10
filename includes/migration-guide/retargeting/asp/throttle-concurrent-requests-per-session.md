### <a name="throttle-concurrent-requests-per-session"></a>Einschränken von gleichzeitigen Anforderungen pro Sitzung

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2 und früher, führt ASP.NET Anforderungen mit der gleichen Sessionid sequenziell aus, und ASP.NET stellt immer die Sessionid mithilfe von Cookies standardmäßig. Wenn eine Seite lange Antworten ausgeführt wird, wird sie serverleistung erheblich beeinträchtigt, einfach durch Drücken von F5 im Browser. Die Lösung haben wir einen Zähler, um die in der Warteschlange Anforderungen nachzuverfolgen und die Anforderungen zu beenden, wenn sie einen bestimmten Grenzwert überschreiten hinzugefügt. Der Standardwert ist 50. Wenn der Grenzwert erreicht ist, wird eine Warnung im Ereignisprotokoll Protokoll- und eine HTTP 500-Antwort im IIS-Protokoll aufgezeichnet werden möglicherweise protokolliert.|
|Vorschlag|Um das alte Verhalten wiederherzustellen, können Sie Ihrer web.config-Datei die folgende Einstellung hinzufügen, um sich gegen das neue Verhalten zu entscheiden.<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7|
|Typ|Neuzuweisung|

