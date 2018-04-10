### <a name="deadlock-may-result-when-using-reentrant-services"></a>Möglicherweise ein Deadlock bei Verwendung von Reentrant services

|   |   |
|---|---|
|Details|Ein Deadlock kann in einem Wiedereintrittsfähige Dienst zurückgeben, was die Instanzen des Diensts auf der Ausführung jeweils einen Thread beschränkt. Dienste, die anfällig für dieses Problem auftritt, verfügen über die folgenden <xref:System.ServiceModel.ServiceBehaviorAttribute> in ihrem Code:<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|Vorschlag|Um dieses Problem zu beheben, können Sie Folgendes tun:<ul><li>Legen Sie die dienstparallelitätsmodus auf <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> oder &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;. Zum Beispiel:</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>Installieren Sie das neueste Update für .NET Framework 4.6.2, oder ein upgrade auf eine höhere Version von .NET Framework. Dies deaktiviert den Ablauf von der <xref:System.Threading.ExecutionContext> in <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>. Dieses Verhalten ist konfigurierbar. Dies ist äquivalent zum folgenden app-Einstellung zu Ihrer Konfigurationsdatei hinzufügen:</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.6.2|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

