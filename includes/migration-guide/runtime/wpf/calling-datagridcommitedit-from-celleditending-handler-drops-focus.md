### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>Aufrufen von DataGrid.CommitEdit von einem Handler CellEditEnding löscht den Fokus

|   |   |
|---|---|
|Details|Aufrufen von <xref:System.Windows.Controls.DataGrid.CommitEdit> aus einer der der <xref:System.Windows.Controls.DataGrid?displayProperty=name>des <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> -Ereignishandler bewirkt, dass die <xref:System.Windows.Controls.DataGrid?displayProperty=name> den Fokus verliert.|
|Vorschlag|Dieses Problem wurde in .NET Framework 4.5.2 behoben, daher kann es durch ein Upgrade von .NET Framework vermieden werden. Sie können alternativ vermieden werden, indem Sie explizit erneut auswählen der <xref:System.Windows.Controls.DataGrid?displayProperty=name> nach dem Aufruf <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

