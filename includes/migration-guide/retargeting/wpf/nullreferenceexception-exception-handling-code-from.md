### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException in Ausnahmebehandlungscode aus ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Details|Fehler im Code für die Ausnahmebehandlung <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> verursacht eine falsche <xref:System.NullReferenceException?displayProperty=name> nicht mit der gewünschten Ausnahme ausgelöst wird (z. B. <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), diese Änderung korrigiert diese Fehler, damit die Methode löst nun die richtige Ausnahme aus. Durch alle Anwendungen, die auf .NET Framework 4.6.2 Standard und im folgenden wird weiterhin auslösen <xref:System.NullReferenceException?displayProperty=name> für Entwickler für .NET Framework 4.7-Kompatibilität und höher sollten finden Sie unter den richtigen exceptions.// Ersetzen mit einem 'X' ggf.|
|Vorschlag|So erhalten Sie zurückkehren möchten Entwickler <xref:System.NullReferenceException?displayProperty=name> Wenn als Ziel .NET Framework 4.7 kann hinzufügen ' / ' Merge Folgendes verwenden, um ihre Anwendung App.config-Datei:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

