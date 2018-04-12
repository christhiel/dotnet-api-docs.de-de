### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a><span data-ttu-id="dd14f-101">Icon.ToBitmap konvertiert Symbole mit PNG-Bildern erfolgreich in Bitmap-Objekte</span><span class="sxs-lookup"><span data-stu-id="dd14f-101">Icon.ToBitmap successfully converts icons with PNG frames into Bitmap objects</span></span>

|   |   |
|---|---|
|<span data-ttu-id="dd14f-102">Details</span><span class="sxs-lookup"><span data-stu-id="dd14f-102">Details</span></span>|<span data-ttu-id="dd14f-103">Angefangen bei den apps, die auf .NET Framework 4.6 abzielen die <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> erfolgreich konvertiert die Symbole mit PNG Bitmap-Objekte. In apps, die auf .NET Framework 4.5.2 und frühere Versionen abzielen die <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> -Methode löst eine <xref:System.ArgumentOutOfRangeException> -Ausnahme aus, wenn das Symbol "-Objekt PNG-Bilder hat. Diese Änderung betrifft apps, die auf .NET Framework 4.6 auszurichten neu kompiliert werden und die spezielle Behandlung implementieren, die <xref:System.ArgumentOutOfRangeException> , die ausgelöst wird, wenn ein Symbol-Objekt PNG-Bilder aufweist.</span><span class="sxs-lookup"><span data-stu-id="dd14f-103">Starting with the apps that target the .NET Framework 4.6, the <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> method successfully converts icons with PNG frames into Bitmap objects.In apps that target the .NET Framework 4.5.2 and earlier versions, the  <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> method throws an <xref:System.ArgumentOutOfRangeException> exception if the Icon object has PNG frames.This change affects apps that are recompiled to target the .NET Framework 4.6 and that implement special handling for the <xref:System.ArgumentOutOfRangeException> that is thrown when an Icon object has PNG frames.</span></span> <span data-ttu-id="dd14f-104">Bei der Ausführung unter .NET Framework 4.6 wird die Konvertierung erfolgreich durchgeführt und eine <xref:System.ArgumentOutOfRangeException> wird nicht mehr ausgelöst. Daher wird der Ausnahmehandler nicht mehr aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd14f-104">When running under the .NET Framework 4.6, the conversion is successful, an <xref:System.ArgumentOutOfRangeException> is no longer thrown, and therefore the exception handler is no longer invoked.</span></span>|
|<span data-ttu-id="dd14f-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="dd14f-105">Suggestion</span></span>|<span data-ttu-id="dd14f-106">Wenn dieses Verhalten nicht erwünscht ist, können Sie das vorherige Verhalten beibehalten, indem Sie das folgende Element zum Hinzufügen der <code>&lt;runtime&gt;</code> -Abschnitt Ihrer "App.config"-Datei:</span><span class="sxs-lookup"><span data-stu-id="dd14f-106">If this behavior is undesirable, you can retain the previous behavior by adding the following element to the <code>&lt;runtime&gt;</code> section of your app.config file:</span></span><pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre><span data-ttu-id="dd14f-107">Wenn die Datei "App.config" bereits enthält die <code>AppContextSwitchOverrides</code> Element, der neue Wert zusammengeführt werden sollen, mit der Value-Attribut, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dd14f-107">If the app.config file already contains the <code>AppContextSwitchOverrides</code> element, the new value should be merged with the value attribute like this:</span></span><pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="dd14f-108">Bereich</span><span class="sxs-lookup"><span data-stu-id="dd14f-108">Scope</span></span>|<span data-ttu-id="dd14f-109">Gering</span><span class="sxs-lookup"><span data-stu-id="dd14f-109">Minor</span></span>|
|<span data-ttu-id="dd14f-110">Version</span><span class="sxs-lookup"><span data-stu-id="dd14f-110">Version</span></span>|<span data-ttu-id="dd14f-111">4.6</span><span class="sxs-lookup"><span data-stu-id="dd14f-111">4.6</span></span>|
|<span data-ttu-id="dd14f-112">Typ</span><span class="sxs-lookup"><span data-stu-id="dd14f-112">Type</span></span>|<span data-ttu-id="dd14f-113">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="dd14f-113">Retargeting</span></span>|
|<span data-ttu-id="dd14f-114">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="dd14f-114">Affected APIs</span></span>|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|
