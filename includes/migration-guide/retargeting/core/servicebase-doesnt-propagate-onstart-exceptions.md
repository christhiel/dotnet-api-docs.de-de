### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase OnStart-Ausnahmen nicht weitergegeben werden.

|   |   |
|---|---|
|Details|In der .NET Framework 4.7 und früheren Versionen werden beim Start des Diensts ausgelöste Ausnahmen nicht an den Aufrufer des weitergegeben <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>. Beginnend mit Anwendungen, die auf .NET Framework 4.7.1 abzielen, verteilt die Runtime Ausnahmen <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> für Dienste, die nicht gestartet werden.|
|Vorschlag|Auf "Dienst starten" Wenn eine Ausnahme auftritt, wird diese Ausnahme weitergegeben werden. Dies soll dabei helfen, Fällen diagnostizieren, in denen Dienste nicht gestartet. Wenn dieses Verhalten nicht erwünscht ist, Sie können abwählen es durch das Hinzufügen der folgenden <AppContextSwitchOverrides> Element an der <runtime> Abschnitt der Konfigurationsdatei der Anwendung:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>Wenn Ihre Anwendung für eine frühere Version als 4.7.1 diejenige, aber dieses Verhalten aufweisen sollen, fügen Sie die folgenden <AppContextSwitchOverrides> Element an der <runtime> Abschnitt der Konfigurationsdatei der Anwendung:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

