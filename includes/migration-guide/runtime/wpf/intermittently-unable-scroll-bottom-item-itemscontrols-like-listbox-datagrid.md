### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>Führen Sie einen Bildlauf zum unteren-Element in ItemsControls (z. B. ListBox-Steuerelement und dem DataGrid) kann zeitweise nicht bei Verwendung von benutzerdefinierten DataTemplates

|   |   |
|---|---|
|Details|In einigen Fällen verursacht ein Fehler in .NET Framework 4.5 ItemsControls (z. B. <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>usw.), nicht auf ihre unteren-Element zu scrollen, bei Verwendung von benutzerdefinierten DataTemplates. Wenn der Vorgang ein zweites Mal versucht wird (nachdem wieder nach oben gescrollt wurde), funktioniert es entsprechend.|
|Vorschlag|Dieses Problem wurde in .NET Framework 4.5.2 behoben und kann durch ein Upgrade auf diese (oder eine höhere) Version von .NET Framework vermieden werden. Alternativ können Benutzer weiterhin Scrolleisten in diesen Auflistungen ziehen, wobei sie es möglicherweise zweimal versuchen müssen, bis der Vorgang erfolgreich ausgeführt wird.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|

