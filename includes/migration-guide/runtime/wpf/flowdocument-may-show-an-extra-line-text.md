### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument möglicherweise eine zusätzliche Textzeile angezeigt.

|   |   |
|---|---|
|Details|In einigen Fällen ein <xref:System.Windows.Documents.FlowDocument> Element wird eine zusätzliche Textzeile angezeigt, bei der Ausführung in .NET Framework 4.5 verglichen, wie es bei Ausführung auf .NET Framework 4.0. Es sind keine bekannten Fällen über die Änderung verursacht eine Verschlechterung der Leistung oder unleserlich, weil anzuzeigende Text, aber es kann dazu führen, dass Text angezeigt werden, die zuvor aus weggelassen wurde eine <xref:System.Windows.Documents.FlowDocument>des anzeigen.|
|Vorschlag|In einigen Fällen kann die Anzeigeelements PageHeight-Eigenschaft nimmt einen die vergangenen Anzahl von Zeilen angezeigt wiederherstellen.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

