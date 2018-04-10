### <a name="glyphruncomputeinkboundingbox-and-formattedtextextent-return-different-values-beginning-in-net-45"></a>GlyphRun.ComputeInkBoundingBox() und FormattedText.Extent geben andere Werte, die ab .NET 4.5 zurück.

|   |   |
|---|---|
|Details|Es wurden Verbesserungen vorgenommen <xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox> und <xref:System.Windows.Media.FormattedText.Extent> in .NET Framework 4.5, um Probleme zu behandeln, in denen die Felder zu klein für die eigenständige Symbole in einigen Fällen in .NET Framework 4.0 wurden. Aus diesem Grund sind einige Begrenzungsrahmen in .NET Framework 4.5 größer, sodass sich geringfügige Unterschiede beim Layout der Benutzeroberfläche ergeben.|
|Vorschlag|Beachten Sie, dass einige Begrenzungsrahmen für Glyphen vergrößert wurden. Diese Änderungen verbessert in der Regel die Darstellung und das Testen von Feldtreffern, aber wenn das ältere Verhalten (vor .NET 4.5) gewünscht wird, kann es durch Hinzufügen des folgenden Eintrags zur Datei „app.config“ aktiviert werden:<pre><code class="language-xml">&lt;appsettings&gt;&#13;&#10;&lt;add key=&quot;IncludeAllInkInBoundingBox&quot; value=&quot;false&quot;&gt;&#13;&#10;&lt;/appsettings&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox?displayProperty=nameWithType></li><li><xref:System.Windows.Media.FormattedText.Extent?displayProperty=nameWithType></li></ul>|

