### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>Durchführen eines Bildlaufs einen WPF TreeView oder der gruppierten ListBox in einem VirtualizingStackPanel kann bewirken, dass ein hängen

|   |   |
|---|---|
|Details|In der .NET Framework 4.5 Durchführen eines Bildlaufs eine WPF <xref:System.Windows.Controls.TreeView?displayProperty=name> in einer virtualisierten Stapel kann Bereich Systemstillstand verursachen, wenn in den Viewport Ränder vorhanden sind (zwischen den Elementen in der <xref:System.Windows.Controls.TreeView?displayProperty=name>, z. B. oder auf einem ItemsPresenter-Element). Darüber hinaus können in einigen Fällen Elemente unterschiedlicher Größe in der Ansicht zur Instabilität führen, auch wenn keine Ränder vorhanden sind.|
|Vorschlag|Dieser Fehler kann durch ein Upgrade auf .NET Framework 4.5.1 vermieden werden. Alternativ können Ränder aus Sicht Sammlungen entfernt werden (z. B. <xref:System.Windows.Controls.TreeView?displayProperty=name>s) in virtualisierten Stapel Panels, wenn alle Elemente haben die gleiche Größe.|
|Bereich|Hauptversion|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

