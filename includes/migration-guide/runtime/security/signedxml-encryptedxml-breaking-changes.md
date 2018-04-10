### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml und EncryptedXml wichtige Änderungen

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2 Sicherheitsupdates <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> und <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> zu verschiedenen Laufzeitverhalten. Ein auf ein Objekt angewendeter<ul><li>Wenn ein Dokument mehrere Elemente mit dem gleichen verfügt <code>id</code> Attribut und einer Signatur auf eines dieser Elemente als Stammverzeichnis für die Signatur ausgerichtet ist, das Dokument wird jetzt werden als ungültig betrachtet.</li><li>Dokumente, die mit nicht-kanonische XPath-Transformation Algorithmen in Verweise sind jetzt als ungültig betrachtet.</li><li>Dokumente, die mit nicht-kanonische XSLT-Transformation Algorithmen in Verweise sind nun sehen wir uns ungültig.</li><li>Alle Anwendung und Nutzen von externen Ressourcen getrennt Signaturen werden nicht möglich.</li></ul>|
|Vorschlag|Entwickler möchten vielleicht überprüfen die Verwendung von <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> und <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>sowie von abgeleitete Typen <xref:System.Security.Cryptography.Xml.Transform> seit ein Dokument Empfänger nicht verarbeitet werden kann.|
|Bereich|Gering|
|Version|4.6.2|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

