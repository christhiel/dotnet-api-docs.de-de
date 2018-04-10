### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Verändertes Verhalten für Task.WaitAll-Methoden mit Timeout-Argumenten

|   |   |
|---|---|
|Details|Task.WaitAll Verhalten, wurde in .NET 4.5.In .NET Framework 4, dieser Methoden inkonsistent erwies konsistenter versucht. Wenn vor dem abgelaufenen Timeoutintervall eine oder mehrere Aufgaben vor dem Methodenaufruf abgeschlossen oder abgebrochen wurden, löste die Methode eine <xref:System.AggregateException?displayProperty=name>-Ausnahme aus. Wenn vor dem abgelaufenen Timeoutintervall keine Aufgaben vor dem Methodenaufruf abgeschlossen oder abgebrochen wurden, aber eine oder mehrere Aufgaben nach dem Methodenaufruf in diesen Zustand eingetreten waren, gab die Methode „false“ zurück.<br/><br/>In .NET Framework 4.5, diese methodenüberladungen jetzt "false" zurückgeben, wenn alle Aufgaben ausgeführt werden, wenn das Timeoutintervall abgelaufen ist, und sie lösen eine <xref:System.AggregateException?displayProperty=name> Ausnahme nur dann, wenn eine eingabeaufgabe abgebrochen wurde (unabhängig davon, ob er vor oder nach der die Methode war Rufen Sie) und keine anderen Aufgaben mehr ausgeführt werden.|
|Vorschlag|Wenn ein <xref:System.AggregateException?displayProperty=name> wurde als Mittel zum Erkennen von einer Aufgabe, die vor dem WaitAll-Aufruf, der aufgerufen wird, abgebrochen wurde, dass Code stattdessen die gleiche Erkennung über die Eigenschaft IsCanceled vorgegangen abgefangen wird (z. B.:. Any(t =&gt; t.IsCanceled)) seit .NET 4.6 wird nur in diesem Fall auslösen, wenn alle erwartete Aufgaben vor dem Timeout abgeschlossen werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

