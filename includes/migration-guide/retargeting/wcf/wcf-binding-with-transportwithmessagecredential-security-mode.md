### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>WCF-Bindung mit den TransportWithMessageCredential-Sicherheitsmodus

|   |   |
|---|---|
|Details|Ab .NET Framework 4.6.1, WCF-Bindung, die den TransportWithMessageCredential-Sicherheitsmodus verwendet kann eingerichtet sein, dass zum Empfangen von Nachrichten nicht signierten &quot;auf&quot; Header für asymmetrische Sicherheitsschlüssel. Standardmäßig unsigniert &quot;auf&quot; Header werden weiterhin in .NET 4.6.1 abgelehnt werden. Sie werden nur akzeptiert werden, wenn eine Anwendung in dieser neue Modus des Vorgangs mit dem Switch.System.ServiceModel.AllowUnsignedToHeader Konfigurationsschalter "OPTS". Da dies eine opt-in-Funktion ist, sollte sie nicht das Verhalten vorhandener Apps auswirken.|
|Vorschlag|Da diese Einstellung eine Opt-in-Funktion ist, sollte sie sich nicht auf das Verhalten vorhandener Apps auswirken. Verwenden Sie die folgende Konfigurationseinstellung, um zu steuern, ob das neue Verhalten oder nicht verwendet wird:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Transparent|
|Version|4.6.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

