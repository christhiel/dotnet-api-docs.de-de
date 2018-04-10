### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap konvertiert Symbole mit PNG-Bildern erfolgreich in Bitmap-Objekte

|   |   |
|---|---|
|Details|Angefangen bei den apps, die auf .NET Framework 4.6 abzielen die <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> erfolgreich konvertiert die Symbole mit PNG Bitmap-Objekte. In apps, die auf .NET Framework 4.5.2 und frühere Versionen abzielen die <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> -Methode löst eine <xref:System.ArgumentOutOfRangeException> -Ausnahme aus, wenn das Symbol "-Objekt PNG-Bilder hat. Diese Änderung betrifft apps, die auf .NET Framework 4.6 auszurichten neu kompiliert werden und die spezielle Behandlung implementieren, die <xref:System.ArgumentOutOfRangeException> , die ausgelöst wird, wenn ein Symbol-Objekt PNG-Bilder aufweist. Bei der Ausführung unter .NET Framework 4.6 wird die Konvertierung erfolgreich durchgeführt und eine <xref:System.ArgumentOutOfRangeException> wird nicht mehr ausgelöst. Daher wird der Ausnahmehandler nicht mehr aufgerufen.|
|Vorschlag|Wenn dieses Verhalten nicht erwünscht ist, können Sie das vorherige Verhalten beibehalten, indem Sie das folgende Element zum Hinzufügen der <code>&lt;runtime&gt;</code> -Abschnitt Ihrer "App.config"-Datei:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Wenn die Datei "App.config" bereits enthält die <code>AppContextSwitchOverrides</code> Element, der neue Wert zusammengeführt werden sollen, mit der Value-Attribut, wie folgt:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.6|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

