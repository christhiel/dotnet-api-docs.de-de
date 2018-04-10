### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>Aufrufen von Items.Refresh an WPF ListBox, ListView oder DataGrid mit der ausgewählten Elemente können dazu führen, dass doppelte Elemente, die im Element angezeigt werden

|   |   |
|---|---|
|Details|In .NET Framework 4.5, ListBox.Items.Refresh aus Code aufrufen, während der Auswahl von Elementen in einem <xref:System.Windows.Controls.ListBox?displayProperty=name> kann dazu führen, dass die ausgewählten Elemente in der Liste dupliziert werden. Ein ähnliches Problem tritt auf, mit <xref:System.Windows.Controls.ListView?displayProperty=name> und <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Dieses Problem wurde in .NET Framework 4.6 behoben.|
|Vorschlag|Dieses Problem kann durch programmgesteuertes aufheben Elemente vor umgangen werden <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> wird aufgerufen, und wählen Sie dann erneut sie nach Abschluss des Aufrufs. Dieses Problem wurde alternativ in .NET Framework 4.6 behoben und kann durch ein Upgrade auf diese Version von .NET Framework vermieden werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

