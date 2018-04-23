### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException im Ausnahmebehandlungscode von ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Details|Durch einen Fehler im Ausnahmebehandlungscode für <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> wurde eine <xref:System.NullReferenceException?displayProperty=name> anstelle der gewünschten Ausnahme ausgelöst (z.B. <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>). Mit dieser Änderung wird dieser Fehler behoben, sodass die Methode nun die richtige Ausnahme auslöst. Standardmäßig lösen alle Anwendungen mit der Zielplattform .NET Framework 4.6.2 und niedriger weiterhin aus Kompatibilitätsgründen <xref:System.NullReferenceException?displayProperty=name> aus. Entwickler, die .NET Framework 4.7 und höher als Zielplattform verwenden, sollten die richtigen Ausnahmen erhalten. //Ersetzen Sie ggf. das Leerzeichen durch ein „x“.|
|Vorschlag|Entwickler, die wieder <xref:System.NullReferenceException?displayProperty=name> erhalten möchten, wenn Sie .NET Framework 4.7 als Zielplattform verwenden, können der Datei „app.config“ ihrer Anwendung Folgendes hinzufügen oder die entsprechenden Angaben zusammenführen:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

