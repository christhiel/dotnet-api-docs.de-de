### <a name="iasyncresultcompletedsynchronously-property-must-be-correct-for-the-resulting-task-to-complete"></a><span data-ttu-id="fc0b1-101">IAsyncResult.CompletedSynchronously-Eigenschaft muss für die resultierende Aufgabe abgeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="fc0b1-101">IAsyncResult.CompletedSynchronously property must be correct for the resulting task to complete</span></span>

|   |   |
|---|---|
|<span data-ttu-id="fc0b1-102">Details</span><span class="sxs-lookup"><span data-stu-id="fc0b1-102">Details</span></span>|<span data-ttu-id="fc0b1-103">Beim Aufrufen von TaskFactory.FromAsync, die Implementierung der <xref:System.IAsyncResult.CompletedSynchronously> -Eigenschaft muss korrekt sein, damit die resultierende Aufgabe abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fc0b1-103">When calling TaskFactory.FromAsync, the implementation of the <xref:System.IAsyncResult.CompletedSynchronously> property must be correct for the resulting task to complete.</span></span> <span data-ttu-id="fc0b1-104">Das heißt, die Eigenschaft muss für den Fall, und ausschließlich für den Fall, dass die Implementierung synchron abgeschlossen wurde, „true“ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fc0b1-104">That is, the property must return true if, and only if, the implementation completed synchronously.</span></span> <span data-ttu-id="fc0b1-105">Zuvor wurde die Eigenschaft nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fc0b1-105">Previously, the property was not checked.</span></span>|
|<span data-ttu-id="fc0b1-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="fc0b1-106">Suggestion</span></span>|<span data-ttu-id="fc0b1-107">Wenn <xref:System.IAsyncResult?displayProperty=name> Implementierungen ordnungsgemäß für "true" Zurückgeben der <xref:System.IAsyncResult.CompletedSynchronously?displayProperty=name> Eigenschaft nur, wenn ein Task synchron abgeschlossen, dann kein Umbruch wird beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="fc0b1-107">If <xref:System.IAsyncResult?displayProperty=name> implementations correctly return true for the <xref:System.IAsyncResult.CompletedSynchronously?displayProperty=name> property only when a task completed synchronously, then no break will be observed.</span></span> <span data-ttu-id="fc0b1-108">Benutzer sollten <xref:System.IAsyncResult?displayProperty=name> Implementierungen deren Besitzer Sie sind (sofern vorhanden) um sicherzustellen, dass sie, ob eine Aufgabe abgeschlossen wird, synchron oder nicht richtig ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="fc0b1-108">Users should review <xref:System.IAsyncResult?displayProperty=name> implementations they own (if any) to ensure that they correctly evaluate whether a task completed synchronously or not.</span></span>|
|<span data-ttu-id="fc0b1-109">Bereich</span><span class="sxs-lookup"><span data-stu-id="fc0b1-109">Scope</span></span>|<span data-ttu-id="fc0b1-110">Edge</span><span class="sxs-lookup"><span data-stu-id="fc0b1-110">Edge</span></span>|
|<span data-ttu-id="fc0b1-111">Version</span><span class="sxs-lookup"><span data-stu-id="fc0b1-111">Version</span></span>|<span data-ttu-id="fc0b1-112">4.5</span><span class="sxs-lookup"><span data-stu-id="fc0b1-112">4.5</span></span>|
|<span data-ttu-id="fc0b1-113">Typ</span><span class="sxs-lookup"><span data-stu-id="fc0b1-113">Type</span></span>|<span data-ttu-id="fc0b1-114">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="fc0b1-114">Retargeting</span></span>|
|<span data-ttu-id="fc0b1-115">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="fc0b1-115">Affected APIs</span></span>|<ul><li><xref:System.Threading.Tasks.TaskFactory.FromAsync(System.IAsyncResult,System.Action{System.IAsyncResult})?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync(System.IAsyncResult,System.Action{System.IAsyncResult},System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync(System.IAsyncResult,System.Action{System.IAsyncResult},System.Threading.Tasks.TaskCreationOptions,System.Threading.Tasks.TaskScheduler)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.IAsyncResult,System.Func{System.IAsyncResult,%60%600})?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync(System.Func{System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync(System.Func{System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.Func{%60%600,System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},%60%600,System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.Func{%60%600,System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},%60%600,System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.Func{System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%600},System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.Func{System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%600},System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.IAsyncResult,System.Func{System.IAsyncResult,%60%600},System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%601(System.IAsyncResult,System.Func{System.IAsyncResult,%60%600},System.Threading.Tasks.TaskCreationOptions,System.Threading.Tasks.TaskScheduler)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%602(System.Func{%60%600,%60%601,System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},%60%600,%60%601,System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%602(System.Func{%60%600,%60%601,System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},%60%600,%60%601,System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%602(System.Func{%60%600,System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%601},%60%600,System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%602(System.Func{%60%600,System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%601},%60%600,System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%603(System.Func{%60%600,%60%601,System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%602},%60%600,%60%601,System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%603(System.Func{%60%600,%60%601,%60%602,System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},%60%600,%60%601,%60%602,System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%603(System.Func{%60%600,%60%601,%60%602,System.AsyncCallback,System.Object,System.IAsyncResult},System.Action{System.IAsyncResult},%60%600,%60%601,%60%602,System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%603(System.Func{%60%600,%60%601,System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%602},%60%600,%60%601,System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%604(System.Func{%60%600,%60%601,%60%602,System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%603},%60%600,%60%601,%60%602,System.Object)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.TaskFactory.FromAsync%60%604(System.Func{%60%600,%60%601,%60%602,System.AsyncCallback,System.Object,System.IAsyncResult},System.Func{System.IAsyncResult,%60%603},%60%600,%60%601,%60%602,System.Object,System.Threading.Tasks.TaskCreationOptions)?displayProperty=nameWithType></li></ul>|
