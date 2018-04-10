### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>WPF-Textfeld Standardwerte Maximum von 100 rückgängig machen

|   |   |
|---|---|
|Details|In .NET 4.5 beträgt der Standardgrenzwert für ein WPF-Textfeld 100 (im Gegensatz zu .NET 4.0, wo der Wert unbegrenzt ist).|
|Vorschlag|Wenn eine Rückgängig-Grenzwert von 100 zu niedrig ist, kann das Limit explizit mit festgelegt werden <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

