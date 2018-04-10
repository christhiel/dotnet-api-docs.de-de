### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>EventListeners ETW-erfassen Ereignisse von Anbietern mit expliziten Schlüsselwörter (z. B. die TPL-Anbieter) nicht

|   |   |
|---|---|
|Details|ETW EventListeners mit leerer Schlüsselwortmaske erfassen Ereignisse von Anbietern mit expliziten Schlüsselwörtern nicht ordnungsgemäß. In .NET Framework 4.5 hat der TPL-Anbieter damit begonnen, explizite Schlüsselwörter bereitzustellen und dadurch dieses Problem ausgelöst. In .NET Framework 4.6 wurde „EventListeners“ aktualisiert, damit dieses Problem nicht mehr auftritt.|
|Vorschlag|Um dieses Problem zu umgehen, ersetzen Sie Aufrufe <xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)> mit Aufrufen an die EnableEvents-Überladung, die explizit angibt der &quot;Schlüsselwörter&quot; Maske verwenden: <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>. Alternativ können Sie dieses Problem wurde in .NET Framework 4.6 behoben und kann durch ein Upgrade auf diese Version von .NET Framework adressiert werden.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

