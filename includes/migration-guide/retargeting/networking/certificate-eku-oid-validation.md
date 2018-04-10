### <a name="certificate-eku-oid-validation"></a>Die Überprüfung des Zertifikats EKU-OID

|   |   |
|---|---|
|Details|Ab .NET Framework 4.6, die <xref:System.Net.Security.SslStream> oder <xref:System.Net.ServicePointManager> Klassen verbesserte Schlüssel verwenden (EKU)-Objekt-ID (OID) Validierung ausführen. Eine erweiterte Schlüsselverwendung (EKU)-Erweiterung ist eine Auflistung von Objektbezeichnern (OIDs), die angeben, die Anwendungen, die den Schlüssel zu verwenden. EKU-OID-Validierung verwendet Remotezertifikat Rückrufe, um sicherzustellen, dass das Remotezertifikat die richtige OIDs für den beabsichtigten Zweck.|
|Vorschlag|Wenn diese Änderung nicht erwünscht ist, können Sie Zertifikat EKU-OID-Überprüfung deaktivieren, indem Sie die folgenden wechseln Sie zum Hinzufügen der [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) in der [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) von Ihrem App-Konfigurationsdatei:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Diese Einstellung wird nur für Abwärtskompatibilität bereitgestellt. Seine Verwendung wird andernfalls nicht empfohlen.</blockquote> |
|Bereich|Gering|
|Version|4.6|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

