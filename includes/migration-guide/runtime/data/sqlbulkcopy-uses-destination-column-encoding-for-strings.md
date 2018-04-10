### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>"SqlBulkCopy" verwendet Ziel Spalte Codierung für Zeichenfolgen

|   |   |
|---|---|
|Details|Beim Einfügen von Daten in eine Spalte verwendet <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> die Codierung der Zielspalte, und nicht die Standardcodierung für <code>VARCHAR</code>- und <code>CHAR</code>-Typen. Diese Änderung schließt die Gefahr einer möglichen Datenbeschädigung aus, die bei Verwenden der Standardcodierung verursacht wird, wenn diese nicht von der Zielspalte verwendet wird. In seltenen Fällen kann möglicherweise eine vorhandene Anwendung eine SqlException-Ausnahme ausgelöst, wenn die Änderung der Codierung Daten, die zu groß erzeugt für die Zielspalte sind.|
|Vorschlag|Erwarten, dass <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> Daten aufgrund der Unterschiede Codierung wird nicht mehr beschädigt. Wenn Zeichenfolgen in der Nähe der Zielspalte Größenlimit kopiert werden, es kann erforderlich sein, entweder Daten (kopiert werden, um zu überprüfen, dass die Daten in der Zielspalte passt) vorab codieren oder catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

