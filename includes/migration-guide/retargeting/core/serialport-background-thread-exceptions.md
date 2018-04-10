### <a name="serialport-background-thread-exceptions"></a>SerialPort Background Threadausnahmen

|   |   |
|---|---|
|Details|Im Hintergrund mit erstellten Threads <xref:System.IO.Ports.SerialPort> Streams beenden den Prozess nicht mehr, wenn OS Ausnahmen ausgelöst werden. In Anwendungen, die .NET Framework 4.7 und frühere Versionen abzielen, ein Prozess beendet wird, wenn eine Betriebssystem-Ausnahme, in einem Hintergrundthread ausgelöst wird mit erstellt eine <xref:System.IO.Ports.SerialPort> Stream. In Anwendungen für .NET Framework 4.7.1 oder eine höhere Version Hintergrundthreads OS Ereignisse gewartet werden im Zusammenhang mit dem aktiven seriellen Anschluss, und in einigen Fällen, z. B. einen plötzlichen Entfernung des seriellen Anschlusses abstürzt.|
|Vorschlag|Für apps, .NET Framework 4.7.1 abzielen, können Sie aus der Ausnahmebehandlung, wenn es nicht erwünscht ist, indem Sie Folgendes hinzufügen Abonnieren der <code>&lt;runtime&gt;</code> Teil Ihrer <code>app.config</code> Datei:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Für apps für frühere Versionen von .NET Framework führen jedoch auf .NET Framework 4.7.1 oder später können Sie dies mit der Ausnahmebehandlung durch Hinzufügen der folgenden Optionen, um die <code>&lt;runtime&gt;</code> Teil Ihrer <code>app.config</code> Datei:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

