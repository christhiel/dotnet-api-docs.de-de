### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>Serialisierung von Steuerzeichen mit DataContractJsonSerializer ist jetzt mit ECMAScript V6 und V8 kompatibel

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2 und früheren Versionen der <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> nicht serialisiert werden einige spezielle Steuerzeichen, wie z. B. \b \f und \t, auf eine Weise, die mit den ECMAScript V6 und V8-Standards kompatibel war. Beginnend mit der .NET Framework-4.7, ist die Serialisierung von diese Steuerzeichen mit ECMAScript V6 und V8 kompatibel.|
|Vorschlag|Für apps, die .NET Framework-4.7 abzielen, ist dieses Feature standardmäßig aktiviert. Wenn dieses Verhalten unerwünscht ist, können Sie sich gegen diese Funktion entscheiden, indem Sie dem Abschnitt <code>&lt;runtime&gt;</code> der app.config- oder web.config-Datei die folgende Zeile hinzufügen:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

