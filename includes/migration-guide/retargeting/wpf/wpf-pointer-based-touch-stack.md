### <a name="wpf-pointer-based-touch-stack"></a><span data-ttu-id="c2d7c-101">WPF-Zeigerbasierten Touch-Stapel</span><span class="sxs-lookup"><span data-stu-id="c2d7c-101">WPF Pointer-Based Touch Stack</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c2d7c-102">Details</span><span class="sxs-lookup"><span data-stu-id="c2d7c-102">Details</span></span>|<span data-ttu-id="c2d7c-103">Diese Änderung fügt die Fähigkeit, eine optionale WM_POINTER ermöglichen WPF Touch/Tablettstift Stapel basierend auf.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-103">This change adds the ability to enable an optional WM_POINTER based WPF touch/stylus stack.</span></span>  <span data-ttu-id="c2d7c-104">Entwickler, die nicht explizit dies aktivieren sollte keine Änderung des Verhaltens der WPF-Touch/Tablettstift angezeigt werden. Bekannte Probleme mit optionalen WM_POINTER aktuelle basierend Touch/Tablettstift Stapel:</span><span class="sxs-lookup"><span data-stu-id="c2d7c-104">Developers that do not explicitly enable this should see no change in WPF touch/stylus behavior.Current Known Issues With optional WM_POINTER based touch/stylus stack:</span></span><ul><li><span data-ttu-id="c2d7c-105">Keine Unterstützung für Freihand in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-105">No support for real-time inking.</span></span></li><li><span data-ttu-id="c2d7c-106">Während der Freihandeingabe StylusPlugins weiterhin funktionieren, und sie verarbeitet werden im UI-Thread was zu Leistungseinbußen führen kann.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-106">While inking and StylusPlugins will still work, they will be processed on the UI Thread which can lead to poor performance.</span></span></li><li><span data-ttu-id="c2d7c-107">Verhaltensänderungen aufgrund von Änderungen bei der heraufstufung von Touch/Stiftereignisse Mausereignisse</span><span class="sxs-lookup"><span data-stu-id="c2d7c-107">Behavioral changes due to changes in promotion from touch/stylus events to mouse events</span></span></li><li><span data-ttu-id="c2d7c-108">Bearbeitung kann sich anders verhalten.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-108">Manipulation may behave differently</span></span></li><li><span data-ttu-id="c2d7c-109">Drag & Drop wird für die Fingereingabe geeignetes Feedback nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-109">Drag/Drop will not show appropriate feedback for touch input</span></span></li><li><span data-ttu-id="c2d7c-110">Dies wirkt sich nicht Stifteingabe</span><span class="sxs-lookup"><span data-stu-id="c2d7c-110">This does not affect stylus input</span></span></li><li><span data-ttu-id="c2d7c-111">Drag & Drop können auf Touch/Stylus-Ereignisse nicht mehr initiiert werden</span><span class="sxs-lookup"><span data-stu-id="c2d7c-111">Drag/Drop can no longer be initiated on touch/stylus events</span></span></li><li><span data-ttu-id="c2d7c-112">Dadurch kann es möglicherweise zu einem Hängen der Anwendung kommen, bis die Mauseingabe erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-112">This can potentially hang the application until mouse input is detected.</span></span></li><li><span data-ttu-id="c2d7c-113">Stattdessen sollten Entwickler Drag & Drop über Mausereignisse einleiten.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-113">Instead, developers should initiate drag and drop from mouse events.</span></span></li></ul>|
|<span data-ttu-id="c2d7c-114">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="c2d7c-114">Suggestion</span></span>|<span data-ttu-id="c2d7c-115">Entwickler, die dieser Stapel aktivieren möchten können hinzufügen/Folgendes verwenden, um ihre "App.config" der Anwendungsdatei ' Merge ':</span><span class="sxs-lookup"><span data-stu-id="c2d7c-115">Developers who wish to enable this stack can add/merge the following to their application's App.config file:</span></span><pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre><span data-ttu-id="c2d7c-116">Entfernen Sie diese, oder Festlegen des Werts auf "false" wird dieser optionalen Stapel deaktivieren. Bitte beachten Sie, dass dieser Stapel nur auf Ersteller-Update für Windows 10 und höher verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c2d7c-116">Removing this or setting the value to false will turn this optional stack off.Please note that this stack is available only on Windows 10 Creators Update and above.</span></span>|
|<span data-ttu-id="c2d7c-117">Bereich</span><span class="sxs-lookup"><span data-stu-id="c2d7c-117">Scope</span></span>|<span data-ttu-id="c2d7c-118">Edge</span><span class="sxs-lookup"><span data-stu-id="c2d7c-118">Edge</span></span>|
|<span data-ttu-id="c2d7c-119">Version</span><span class="sxs-lookup"><span data-stu-id="c2d7c-119">Version</span></span>|<span data-ttu-id="c2d7c-120">4.7</span><span class="sxs-lookup"><span data-stu-id="c2d7c-120">4.7</span></span>|
|<span data-ttu-id="c2d7c-121">Typ</span><span class="sxs-lookup"><span data-stu-id="c2d7c-121">Type</span></span>|<span data-ttu-id="c2d7c-122">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="c2d7c-122">Retargeting</span></span>|
