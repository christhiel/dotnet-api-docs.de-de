### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException legt ordnungsgemäß jetzt Zeile Positionen

|   |   |
|---|---|
|Details|Wenn die <xref:System.Xml.Linq.LoadOptions.SetLineInfo> Wert an das Load-Methode übergeben wird und ein Validierungsfehler auftritt, die <xref:System.Xml.Schema.XmlSchemaException.LineNumber> und <xref:System.Xml.Schema.XmlSchemaException.LinePosition> Eigenschaften enthalten jetzt Zeileninformationen.|
|Vorschlag|Ausnahmebehandlungscode, die annimmt, <xref:System.Xml.Schema.XmlSchemaException.LineNumber> und <xref:System.Xml.Schema.XmlSchemaException.LinePosition> nicht Satz sollte aktualisiert werden, da diese Eigenschaften jetzt ordnungsgemäß festgelegt werden sollen, wenn SetLineInfo beim Laden von XML verwendet wird.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

