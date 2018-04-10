### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>Geändert von MD5, SHA1 Workflow-Prüfsummen

|   |   |
|---|---|
|Details|Um das Debuggen mit Visual Studio zu unterstützen, generiert die Workflowlaufzeit eine Prüfsumme für eine Workflowinstanz mithilfe eines Hashalgorithmus. In .NET Framework 4.6.2 und früheren Versionen verwendet das Workflow Prüfsumme hashing den MD5-Algorithmus, dies verursachte Probleme auf FIPS-konformen Systemen aus. Beginnend mit der .NET Framework-4.7, wird der Algorithmus SHA1. Wenn Ihr Code diese Prüfsummen persistent gespeichert, werden sie nicht kompatibel.|
|Vorschlag|Wenn Ihr Code kann nicht zum Laden von Workflowinstanzen aufgrund eines Fehlers Prüfsumme ist, versuchen Sie die <code>AppContext</code> wechseln &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; auf "true". Im Code:<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>Oder in der Konfiguration:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7|
|Typ|Neuzuweisung|

