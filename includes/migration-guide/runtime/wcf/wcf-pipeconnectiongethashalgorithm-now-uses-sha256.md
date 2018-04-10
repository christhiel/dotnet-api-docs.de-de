### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF-PipeConnection.GetHashAlgorithm verwendet nun SHA256

|   |   |
|---|---|
|Details|Ab .NET Framework 4.7.1, verwendet Windows Communication Foundation SHA256-Hash zum Generieren von zufälligen Names für named Pipes. In der .NET Framework 4.7 und früheren Versionen wird SHA1-Hash verwendet.|
|Vorschlag|Wenn Kompatibilitätsproblems mit dieser Änderung auf .NET Framework 4.7.1 auftreten oder höher, Sie können Ausschlussverfahren es durch die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> -Abschnitt Ihrer "App.config"-Datei:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7.1|
|Typ|Laufzeit|

