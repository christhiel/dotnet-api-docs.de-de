### <a name="default-signedxml-and-signedxms-algorithms-changed-to-sha256"></a>Standard-SignedXML und SignedXMS Algorithmen SHA256 geändert

|   |   |
|---|---|
|Details|In der .NET Framework-4.7 und früher standardmäßig SignedXML und SignedCMS SHA1 für bestimmte Vorgänge. Ab .NET Framework 4.7.1, wird standardmäßig für diese Vorgänge SHA256 aktiviert werden. Diese Änderung ist erforderlich, da SHA1 nicht mehr sicher ist.|
|Vorschlag|Es gibt zwei neue Kontext Switch Werte steuern, ob SHA1 (unsicheren) oder SHA256 standardmäßig verwendet wird:<ul><li>Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms</li><li>Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms</li></ul>Anwendungen für .NET Framework 4.7.1 und höheren Versionen ist die Verwendung von SHA256 unerwünscht sind Sie standardmäßig in SHA1 wiederherstellen können durch Hinzufügen der folgenden Konfigurations wechseln Sie zu der [Runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) Teil Ihrer app-Konfiguration Datei:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=true;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=true&quot; /&gt;&#13;&#10;</code></pre>Für Anwendungen, die .NET Framework 4.7 und frühere Versionen abzielen, Sie können optional in diese Änderung durch Hinzufügen der folgenden Konfiguration Schalters, der die [Runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) Teil der Datei "App.config":<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=false;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=false&quot; /&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Security.Cryptography.Pkcs.CmsSigner?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.Reference?displayProperty=nameWithType></li></ul>|

