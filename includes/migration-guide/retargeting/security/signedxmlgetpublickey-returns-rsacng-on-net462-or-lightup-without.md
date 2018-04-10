### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey gibt RSACng für net462 (oder Lightup) zurück, ohne die Änderungen der neuzuweisungen

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.6.2, den konkreten Typ des Objekts zurückgegeben wird, indem Sie die <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> Methode geändert (ohne eine Besonderheit) von einem CryptoServiceProvider-Implementierung eine Cng-Implementierung. Dies ist, da die Implementierung von der Verwendung geändert <code>certificate.PublicKey.Key</code> zur Verwendung der internen <code>certificate.GetAnyPublicKey</code> die leitet an <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.|
|Vorschlag|Beginnend mit apps, die auf .NET Framework 4.7.1 ausgeführt wird, können Sie die CryptoServiceProvider-Implementierung, die standardmäßig in .NET Framework 4.6.1 verwendet und frühere Versionen durch Hinzufügen der folgenden Konfigurations wechseln Sie zu der [Runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)Teil der Datei "App.config":<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.6.2|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

