### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a>ListBoxItem IsSelected Bindung Gruppenrichtlinienproblem ObservableCollection&lt;T&gt;. Verschieben

|   |   |
|---|---|
|Details|Aufrufen <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> oder <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> auf eine Auflistung gebunden werden, um eine <xref:System.Windows.Controls.ListBox?displayProperty=name> mit ausgewählten Elementen kann zu fehlerhaften Verhalten bei zukünftigen Auswahl oder Unselection der führen <xref:System.Windows.Controls.ListBox?displayProperty=name> Elemente.|
|Vorschlag|Aufrufen von <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> und <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> anstelle von <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> wird dieses Problem umgehen. Dieses Problem wurde alternativ in .NET Framework 4.6 behoben und kann durch ein Upgrade auf diese Version von .NET Framework vermieden werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

