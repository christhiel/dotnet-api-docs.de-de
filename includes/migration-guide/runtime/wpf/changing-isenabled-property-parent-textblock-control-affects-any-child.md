### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>Ändern der "IsEnabled"-Eigenschaft des übergeordneten Elements ein TextBlock-Steuerelement wirkt sich auf alle untergeordneten Steuerelemente

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.6.2, Ändern der <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> Eigenschaft des übergeordneten Elements einen <xref:System.Windows.Controls.TextBlock?displayProperty=name> Steuerelement wirkt sich auf alle untergeordneten Steuerelemente (z. B. links und Schaltflächen), der die <xref:System.Windows.Controls.TextBlock?displayProperty=name> Steuerelement. In .NET Framework 4.6.1 und früheren Versionen, Steuerelemente innerhalb einer <xref:System.Windows.Controls.TextBlock?displayProperty=name> den Status nicht immer widerspiegeln der <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> Eigenschaft der <xref:System.Windows.Controls.TextBlock?displayProperty=name> übergeordneten.|
|Vorschlag|Keine Diese Änderung entspricht dem erwarteten Verhalten für Steuerelemente innerhalb eines <xref:System.Windows.Controls.TextBlock?displayProperty=name>-Steuerelements.|
|Bereich|Gering|
|Version|4.6.2|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

