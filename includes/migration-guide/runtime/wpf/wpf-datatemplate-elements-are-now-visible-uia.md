### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>WPF-DataTemplate-Elemente sind jetzt für UIA sichtbar

|   |   |
|---|---|
|Details|Zuvor <xref:System.Windows.DataTemplate?displayProperty=name> Elemente wurden für die Automatisierung der Benutzeroberfläche nicht sichtbar. Ab Version 4.5 erkennt die Benutzeroberflächenautomatisierung diese Elemente. Dies ist in vielen Fällen hilfreich, jedoch können die Tests, die von der UIA-Strukturen, die nicht mit abhängen unterbrechen <xref:System.Windows.DataTemplate?displayProperty=name> Elemente.|
|Vorschlag|Benutzeroberflächenautomatisierungs-Tests für diese app möglicherweise aktualisiert, um der UIA-Struktur, die jetzt einschließlich zuvor unsichtbar zu berücksichtigen <xref:System.Windows.DataTemplate?displayProperty=name> Elemente. Beispielsweise müssen Tests, die erwarten, dass einige Elemente nebeneinander angeordnet sind, jetzt möglicherweise davon ausgehen, dass sich zwischen diesen Elementen zuvor unsichtbare UIA-Elemente befinden. Möglicherweise müssen auch Tests mit neuen Werten aktualisiert werden, die auf bestimmte Werte oder Indizes für UIA-Elemente angewiesen sind.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

