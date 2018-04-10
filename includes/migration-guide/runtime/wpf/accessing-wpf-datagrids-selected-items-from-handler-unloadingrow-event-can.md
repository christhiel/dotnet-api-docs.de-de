### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>Zugreifen auf ein WPF-DataGrid ausgewählten Elemente von einem Handler des Ereignisses für das Datenraster UnloadingRow kann bewirken, dass eine NullReferenceException

|   |   |
|---|---|
|Details|Aufgrund eines Fehlers in der .NET Framework 4.5-Ereignishandler für <xref:System.Windows.Controls.DataGrid> Ereignisse im Zusammenhang mit dem Entfernen einer Zeile können dazu führen, dass eine <xref:System.NullReferenceException?displayProperty=name> ausgelöst wird, wenn sie Zugriff auf die <xref:System.Windows.Controls.DataGrid>des <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> oder <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> Eigenschaften.|
|Vorschlag|Dieses Problem behoben wurde in .NET Framework 4.6 und kann durch ein Upgrade auf diese Version von .NET Framework adressiert werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

