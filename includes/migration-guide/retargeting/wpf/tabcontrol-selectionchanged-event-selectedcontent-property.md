### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>TabControl-SelectionChanged-Ereignis und SelectedContent-Eigenschaft

|   |   |
|---|---|
|Details|Ab .NET Framework 4.7.1, eine <xref:System.Windows.Controls.TabControl> aktualisiert den Wert seiner <xref:System.Windows.Controls.TabControl.SelectedContent> Eigenschaft vor dem Auslösen der <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignis, wenn sich die Auswahl ändert. Aufgetreten sind in der .NET Framework 4.7 und früheren Versionen wird das Update auf SelectedContent nach dem Ereignis.|
|Vorschlag|Apps, die die .NET Framework-4.7.1 oder höher können abwählen dies ändern, und Verwenden von Legacyverhalten durch Hinzufügen der folgenden Optionen, um die <code>&lt;runtime&gt;</code> Abschnitt der Konfigurationsdatei der Anwendung:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Apps, die .NET Framework 4.7 oder früheren jedoch abzielen, auf .NET Framework 4.7.1 ausgeführt werden oder höher kann das neue Verhalten durch die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> Abschnitt der Datei .configuration Anwendung:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

