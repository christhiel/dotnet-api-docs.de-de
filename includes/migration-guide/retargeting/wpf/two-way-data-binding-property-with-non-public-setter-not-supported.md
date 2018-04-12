### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a><span data-ttu-id="dcdf6-101">Bidirektionale Datenbindung an eine Eigenschaft mit einem nicht öffentlichen Setter wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-101">Two-way data-binding to a property with a non-public setter is not supported</span></span>

|   |   |
|---|---|
|<span data-ttu-id="dcdf6-102">Details</span><span class="sxs-lookup"><span data-stu-id="dcdf6-102">Details</span></span>|<span data-ttu-id="dcdf6-103">Der Versuch, Daten ohne einen öffentlichen Setter an eine Eigenschaft zu binden, wurde nie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-103">Attempting to data bind to a property without a public setter has never been a supported scenario.</span></span> <span data-ttu-id="dcdf6-104">Ab .NET Framework 4.5.1 ist dieses Szenario löst ein <xref:System.InvalidOperationException?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-104">Beginning in the .NET Framework 4.5.1, this scenario will throw an <xref:System.InvalidOperationException?displayProperty=name>.</span></span> <span data-ttu-id="dcdf6-105">Beachten Sie, dass diese neue Ausnahme nur für Apps ausgelöst wird, die speziell auf .NET Framework 4.5.1 abzielen.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-105">Note that this new exception will only be thrown for apps that specifically target the .NET Framework 4.5.1.</span></span> <span data-ttu-id="dcdf6-106">Wenn eine App auf .NET Framework 4.5 ausgerichtet ist, wird der Aufruf zugelassen.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-106">If an app targets the .NET Framework 4.5, the call will be allowed.</span></span> <span data-ttu-id="dcdf6-107">Wenn die App nicht auf eine bestimmte Version von .NET Framework ausgerichtet ist, wird die Bindung als unidirektionale Bindung behandelt.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-107">If the app does not target a particular .NET Framework version, the binding will be treated as one-way.</span></span>|
|<span data-ttu-id="dcdf6-108">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="dcdf6-108">Suggestion</span></span>|<span data-ttu-id="dcdf6-109">Die App sollte aktualisiert werden, um entweder die unidirektionale Bindung zu verwenden oder den Setter der Eigenschaft öffentlich zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-109">The app should be updated to either use one-way binding, or expose the property's setter publicly.</span></span> <span data-ttu-id="dcdf6-110">Alternativ können Sie die App auf .NET Framework 4.5 ausrichten, um das alte Verhalten zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-110">Alternatively, targeting the .NET Framework 4.5 will cause the app to exhibit the old behavior.</span></span>|
|<span data-ttu-id="dcdf6-111">Bereich</span><span class="sxs-lookup"><span data-stu-id="dcdf6-111">Scope</span></span>|<span data-ttu-id="dcdf6-112">Gering</span><span class="sxs-lookup"><span data-stu-id="dcdf6-112">Minor</span></span>|
|<span data-ttu-id="dcdf6-113">Version</span><span class="sxs-lookup"><span data-stu-id="dcdf6-113">Version</span></span>|<span data-ttu-id="dcdf6-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="dcdf6-114">4.5.1</span></span>|
|<span data-ttu-id="dcdf6-115">Typ</span><span class="sxs-lookup"><span data-stu-id="dcdf6-115">Type</span></span>|<span data-ttu-id="dcdf6-116">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="dcdf6-116">Retargeting</span></span>|
|<span data-ttu-id="dcdf6-117">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="dcdf6-117">Affected APIs</span></span>|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|
