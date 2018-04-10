### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>WCF-nachrichtensicherheit ist jetzt in der Lage, TLS 1.1 und TLS 1.2 verwenden

|   |   |
|---|---|
|Details|Ab der .NET Framework-4.7, können Kunden TLS1.1 oder TLS 1.2 in WCF-nachrichtensicherheit neben SSL 3.0 und TLS 1.0 über die Konfigurationseinstellungen für die Anwendung konfigurieren.|
|Vorschlag|In der .NET Framework-4.7 ist die Unterstützung für TLS 1.1 und TLS 1.2 in WCF-nachrichtensicherheit standardmäßig deaktiviert. Sie können es aktivieren, indem Sie die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> Abschnitt der Datei "App.config" oder "Web.config":<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7|
|Typ|Neuzuweisung|

