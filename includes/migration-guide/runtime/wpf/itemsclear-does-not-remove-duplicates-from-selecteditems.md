### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear werden keine Duplikate aus SelectedItems entfernt.

|   |   |
|---|---|
|Details|Angenommen, ein Selektor (mit Mehrfachauswahl aktiviert) Duplikate hat seiner <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> Auflistung - dasselbe Element wird mehrmals angezeigt.  Entfernen diese Elemente aus der Datenquelle (z. B. durch Aufrufen von Items.Clear) ein Fehler auftritt, entfernen Sie diese aus <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; nur die erste Instanz entfernt wird. Darüber hinaus nachfolgende Verwendung des <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (z. B. SelectedItems.Clear()) kann es zu Problemen wie z. B. <xref:System.ArgumentException?displayProperty=name>, da <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> enthält Elemente, die nicht mehr in der Datenquelle vorhanden sind.|
|Vorschlag|Wenn möglich auf .NET 4.6.2 aktualisieren.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

