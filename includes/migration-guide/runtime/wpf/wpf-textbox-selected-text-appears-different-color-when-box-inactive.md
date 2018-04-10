### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>WPF-Textfeld ausgewählten Text wird einer anderen Farbe angezeigt, wenn das Textfeld aktiv ist

|   |   |
|---|---|
|Details|Wenn in .NET 4.5 ein WPF-Textfeldsteuerelement inaktiv ist (nicht den Fokus besitzt), wird der im Feld markierte Text in einer anderen Farbe als bei einem aktiven Steuerelement angezeigt.|
|Vorschlag|Vorherige (.NET 4.0)-Verhalten kann wiederhergestellt werden, durch Festlegen der <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> Eigenschaft <code>false</code>.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

