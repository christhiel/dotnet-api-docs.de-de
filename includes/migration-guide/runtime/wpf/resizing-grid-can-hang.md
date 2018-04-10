### <a name="resizing-a-grid-can-hang"></a>Ändern der Größe von einem Raster kann hängen.

|   |   |
|---|---|
|Details|Eine Endlosschleife auftreten kann, während des Layouts von einem <code>T:System.Windows.Controls.Grid</code> in den folgenden Situationen:<ul><li>Zeilendefinitionen enthalten zwei *-Zeilen, die beide eine MinHeight und eine MaxHeight deklariert.</li><li>Der Inhalt der *-Zeilen nicht die entsprechenden MaxHeight überschreiten</li><li>Verfügbare Rasterhöhe durch den ersten MinHeight überschritten (plus alle anderen festen oder automatisch Zeilen)</li><li>Die app als Ziel verwendet .net 4.7 oder durch Festlegen von für die Teilnahme an der 4.7 Zuordnungsalgorithmus <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>Die Schleife ist auch mit mehr als zwei Zeilen oder in der analoge Groß-/Kleinschreibung für Spalten der Fall. Das Problem ist in .net 4.7.1 behoben.|
|Vorschlag|Upgrade auf .net 4.7.1.  Wenn Sie den 4.7 Zuordnungsalgorithmus benötigen können Sie die folgende Konfigurationseinstellung verwenden:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7|
|Typ|Laufzeit|

