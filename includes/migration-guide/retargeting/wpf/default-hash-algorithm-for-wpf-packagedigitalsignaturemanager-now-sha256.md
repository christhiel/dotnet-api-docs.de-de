### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>Der Standardhashalgorithmus für WPF-PackageDigitalSignatureManager ist jetzt SHA256

|   |   |
|---|---|
|Details|Die <code>System.IO.Packaging.PackageDigitalSignatureManager</code> stellt Funktionen für digitale Signaturen in Bezug auf WPF-Paketen bereit.  In der .NET Framework 4.7 und früheren Versionen ist der Standardalgorithmus (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) SHA1 zum Signieren der Teile eines Pakets verwendet wurde.  Aufgrund der aktuellen Sicherheitsaspekte mit SHA1, diesen Standardwert in SHA256 geändert wurde mit .NET Framework 4.7.1 ab.  Diese Änderung betrifft alle paketsignierung, einschließlich der XPS-Dokumente.|
|Vorschlag|Ein Entwickler, die diese Änderung beim Abzielen auf ein Frameworkversion unter .NET 4.7.1 nutzen möchte oder ein Entwickler, der die vorherige Funktionalität beim Abzielen auf .NET 4.7.1 oder höher kann muss festgelegt das folgende AppContext Flag entsprechend.  Der Wert "true" führt zu SHA1 als den standardmäßigen-Algorithmus verwendet wird "false" / / ergibt SHA256.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

