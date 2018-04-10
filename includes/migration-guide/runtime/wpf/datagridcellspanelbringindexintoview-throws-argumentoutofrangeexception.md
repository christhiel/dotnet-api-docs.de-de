### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView löst ArgumentOutOfRangeException

|   |   |
|---|---|
|Details|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> funktionieren asynchron bei Spaltenvirtualisierung ist aktiviert, aber die jeweilige Spaltenbreite noch nicht festgelegt wurden.  Wenn Spalten entfernt werden, bevor der asynchrone Vorgang erfolgt, ein <xref:System.ArgumentOutOfRangeException?displayProperty=name> auftreten können.|
|Vorschlag|Eine der folgenden:<ol><li>Upgrade auf .NET 4.7.</li><li>Installieren Sie den neuesten Wartung Patch für .NET 4.6.2.</li><li>Vermeiden Sie Spalten entfernen, bis die asynchrone Antwort auf <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> abgeschlossen wurde.</li></ol>|
|Bereich|Edge|
|Version|4.6.2|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

