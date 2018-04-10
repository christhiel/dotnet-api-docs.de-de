### <a name="xslt-style-sheet-exception-message-changed"></a>XSLT-Stylesheet Ausnahmemeldung geändert

|   |   |
|---|---|
|Details|In .NET Framework 4.5, wird der Text der Fehlermeldung, wenn eine XSLT-Datei zu komplex ist &quot;das Stylesheet ist zu komplex.&quot; In früheren Versionen wurde die Fehlermeldung &quot;XSLT Kompilierungsfehler.&quot; Anwendungscode, der vom Text der Fehlermeldung abhängt, funktioniert nicht mehr. Die Ausnahmetypen sind jedoch nach wie vor identisch, daher sollte diese Änderung keine tatsächlichen Auswirkungen haben.|
|Vorschlag|Aktualisieren des app-Code je nach der Ausnahmemeldung aus diesen Fehlerzustand zu erwarten, dass die neue Nachricht, oder (sogar) aktualisieren Sie den Code so, dass nur der Typ der Ausnahme abhängig (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), die nicht geändert wurde.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

