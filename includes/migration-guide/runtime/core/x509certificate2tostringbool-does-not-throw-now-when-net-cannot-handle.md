### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) löst jetzt bei .NET das Zertifikat nicht verarbeiten kann

|   |   |
|---|---|
|Details|Zuvor, würde dieser Methode auslösen, wenn <code>true</code> für von den verbose-Parameter übergeben wurde, und es sind Zertifikate installiert, die von .NET Framework unterstützt nicht waren. Nun wird die Methode erfolgreich ausgeführt werden und eine gültige Zeichenfolge, die die kann nicht zugegriffen werden Teile des Zertifikats lässt zurückgeben.|
|Vorschlag|Jeder Code je nach <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> aktualisiert werden soll, wenn Sie erwarten, dass einige Zertifikatdaten (z. B. öffentlichen Schlüssel, privaten Schlüssel und Erweiterungen) zurückgegebene Zeichenfolge ausschließen, möglicherweise in einigen Fällen in der die API zuvor ausgelöst haben würden.|
|Bereich|Edge|
|Version|4.6|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

