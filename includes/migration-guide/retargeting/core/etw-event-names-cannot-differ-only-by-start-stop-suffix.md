### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>ETW-Ereignisnamen dürfen sich nicht nur durch ein Suffix "Start" oder "Beenden" unterscheiden.

|   |   |
|---|---|
|Details|In .NET Framework 4.6 und 4.6.1, löst die Laufzeit eine <xref:System.ArgumentException> Wenn zwei Ereignis Ereignisablaufverfolgung für Windows (ETW) Ereignisnamen unterscheiden nur von einem &quot;starten&quot; oder &quot;beenden&quot; Suffix (als bei einem Ereignis heißt<code>LogUser</code>und einen anderen Namen <code>LogUserStart</code>). In diesem Fall kann die Runtime die Ereignisquelle nicht erstellen, die dann keine Protokollierung durchführen kann.|
|Vorschlag|Um die Ausnahme zu vermeiden, stellen Sie sicher, dass keine zwei Ereignisnamen unterscheiden, die nur von einem &quot;starten&quot; oder &quot;beenden&quot; Suffix. Diese Anforderung entfernt wird, beginnend mit .NET Framework 4.6.2. die Common Language Runtime kann Ereignisnamen, die sich nur durch unterscheiden eindeutig die &quot;starten&quot; und &quot;beenden&quot; Suffix.|
|Bereich|Edge|
|Version|4.6|
|Typ|Neuzuweisung|

