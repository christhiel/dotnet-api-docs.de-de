### <a name="long-path-support"></a>Unterstützung für lange Pfade

|   |   |
|---|---|
|Details|Beginnend mit apps, die auf .NET Framework 4.6.2, lange Pfade (der bis zu 32 K-Zeichen) werden unterstützt, und die 260-Zeichen (oder <code>MAX_PATH</code>) Einschränkung in Bezug auf die Länge des Pfads entfernt wurde. Für apps, die neu kompiliert werden, die .NET Framework 4.6.2, Codepfade, die zuvor ausgelöst hat eine <xref:System.IO.PathTooLongException?displayProperty=name> ein Pfad überschritten 260 Zeichen enthalten jetzt löst eine <xref:System.IO.PathTooLongException?displayProperty=name> nur unter folgenden Bedingungen:<ul><li>Die Länge des Pfads ist größer als <xref:System.Int16.MaxValue> (32.767) Zeichen.</li><li>Das Betriebssystem gibt <code>COR_E_PATHTOOLONG</code> oder einen dazu äquivalenten Wert zurück.</li></ul>Für apps, die .NET Framework 4.6.1 und frühere Versionen abzielen, löst die Laufzeit automatisch eine <xref:System.IO.PathTooLongException?displayProperty=name> immer ein Pfad 260 Zeichen überschreitet.|
|Vorschlag|Für apps, die das .NET 4.6.2 Framework, Sie können abwählen Unterstützung langer Pfad, wenn es nicht erwünscht ist, durch das Hinzufügen der folgenden an der <code>&lt;runtime&gt;</code> Teil Ihrer <code>app.config</code> Datei:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Für apps für frühere Versionen von .NET Framework führen jedoch auf .NET Framework 4.6.2 oder höher können Sie abonnieren zur Unterstützung von Langer Pfad durch das Hinzufügen der folgenden an der <code>&lt;runtime&gt;</code> Teil Ihrer <code>app.config</code> Datei:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.6.2|
|Typ|Neuzuweisung|

