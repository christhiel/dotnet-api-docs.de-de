### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a><span data-ttu-id="e16a8-101">Verändertes Verhalten für Task.WaitAll-Methoden mit Timeout-Argumenten</span><span class="sxs-lookup"><span data-stu-id="e16a8-101">Change in behavior for Task.WaitAll methods with time-out arguments</span></span>

|   |   |
|---|---|
|<span data-ttu-id="e16a8-102">Details</span><span class="sxs-lookup"><span data-stu-id="e16a8-102">Details</span></span>|<span data-ttu-id="e16a8-103">Task.WaitAll Verhalten, wurde in .NET 4.5.In .NET Framework 4, dieser Methoden inkonsistent erwies konsistenter versucht.</span><span class="sxs-lookup"><span data-stu-id="e16a8-103">Task.WaitAll behavior was made more consistent in .NET 4.5.In the .NET Framework 4, these methods behaved inconsistently.</span></span> <span data-ttu-id="e16a8-104">Wenn vor dem abgelaufenen Timeoutintervall eine oder mehrere Aufgaben vor dem Methodenaufruf abgeschlossen oder abgebrochen wurden, löste die Methode eine <xref:System.AggregateException?displayProperty=name>-Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="e16a8-104">When the time-out expired, if one or more tasks were completed or canceled before the method call, the method threw an <xref:System.AggregateException?displayProperty=name> exception.</span></span> <span data-ttu-id="e16a8-105">Wenn vor dem abgelaufenen Timeoutintervall keine Aufgaben vor dem Methodenaufruf abgeschlossen oder abgebrochen wurden, aber eine oder mehrere Aufgaben nach dem Methodenaufruf in diesen Zustand eingetreten waren, gab die Methode „false“ zurück.</span><span class="sxs-lookup"><span data-stu-id="e16a8-105">When the time-out expired, if no tasks were completed or canceled before the method call, but one or more tasks entered these states after the method call, the method returned false.</span></span><br/><br/><span data-ttu-id="e16a8-106">In .NET Framework 4.5, diese methodenüberladungen jetzt "false" zurückgeben, wenn alle Aufgaben ausgeführt werden, wenn das Timeoutintervall abgelaufen ist, und sie lösen eine <xref:System.AggregateException?displayProperty=name> Ausnahme nur dann, wenn eine eingabeaufgabe abgebrochen wurde (unabhängig davon, ob er vor oder nach der die Methode war Rufen Sie) und keine anderen Aufgaben mehr ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e16a8-106">In the .NET Framework 4.5, these method overloads now return false if any tasks are still running when the time-out interval expired, and they throw an <xref:System.AggregateException?displayProperty=name> exception only if an input task was cancelled (regardless of whether it was before or after the method call) and no other tasks are still running.</span></span>|
|<span data-ttu-id="e16a8-107">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="e16a8-107">Suggestion</span></span>|<span data-ttu-id="e16a8-108">Wenn ein <xref:System.AggregateException?displayProperty=name> wurde als Mittel zum Erkennen von einer Aufgabe, die vor dem WaitAll-Aufruf, der aufgerufen wird, abgebrochen wurde, dass Code stattdessen die gleiche Erkennung über die Eigenschaft IsCanceled vorgegangen abgefangen wird (z. B.:. Any(t =&gt; t.IsCanceled)) seit .NET 4.6 wird nur in diesem Fall auslösen, wenn alle erwartete Aufgaben vor dem Timeout abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e16a8-108">If an <xref:System.AggregateException?displayProperty=name> was being caught as a means of detecting a task that was cancelled prior to the WaitAll call being invoked, that code should instead do the same detection via the IsCanceled property (for example: .Any(t =&gt; t.IsCanceled)) since .NET 4.6 will only throw in that case if all awaited tasks are completed prior to the timeout.</span></span>|
|<span data-ttu-id="e16a8-109">Bereich</span><span class="sxs-lookup"><span data-stu-id="e16a8-109">Scope</span></span>|<span data-ttu-id="e16a8-110">Gering</span><span class="sxs-lookup"><span data-stu-id="e16a8-110">Minor</span></span>|
|<span data-ttu-id="e16a8-111">Version</span><span class="sxs-lookup"><span data-stu-id="e16a8-111">Version</span></span>|<span data-ttu-id="e16a8-112">4.5</span><span class="sxs-lookup"><span data-stu-id="e16a8-112">4.5</span></span>|
|<span data-ttu-id="e16a8-113">Typ</span><span class="sxs-lookup"><span data-stu-id="e16a8-113">Type</span></span>|<span data-ttu-id="e16a8-114">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="e16a8-114">Runtime</span></span>|
|<span data-ttu-id="e16a8-115">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="e16a8-115">Affected APIs</span></span>|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|
