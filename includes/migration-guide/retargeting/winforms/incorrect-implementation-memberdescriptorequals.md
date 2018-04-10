### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Falsche MemberDescriptor.Equals-Implementierung

|   |   |
|---|---|
|Details|Ursprüngliche Implementierung der &quot;gleich&quot; Methode wurde zwei verschiedenen Zeichenfolgen-Eigenschaften aus den Objekten unter Vergleich vergleichen: Kategorienamen zu Beschreibungszeichenfolge. Die Korrektur besteht darin, vergleichen &quot;Kategorie&quot; des ersten Objekts &quot;Kategorie&quot; der zweiten und &quot;Beschreibung&quot; auf &quot;Beschreibung&quot;. Konfigurationswert MemberDescriptorEqualsReturnsFalseIfEquivalent kann festgelegt werden, auf "true", um das neue Verhalten abzuwählen, wenn 4.6.2 Zielobjekte oder auf "false", um diesen Fix zu aktivieren, wenn ansteuern Framework-Version unter 4.6.2 liegt.|
|Vorschlag|MemberDescriptor.Equals manchmal Rückgabe "false" die Anwendung abhängt, wenn Deskriptoren äquivalent sind, und Sie 4.6.2 abzielen Version von .NET Framework gibt es mehrere Möglichkeiten:<ol><li>Stellen Sie die codeänderungen zu vergleichende &quot;Kategorie&quot; und &quot;Beschreibung&quot; Felder manuell neben dem Ausführen von Equals-Methode.</li><li>Keine Teilnahme durch diese Änderung durch den folgenden Wert in der Datei "App.config" hinzufügen:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Wenn Ihre Anwendung Ziele 4.6.1 oder eine niedrigere Version von .NET Framework, und Sie diese Änderung, die aktiviert werden soll, können Sie die Kompatibilitätsschalter auf "false" festlegen, durch den folgenden Wert in der Datei "App.config" hinzufügen:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.6.2|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

