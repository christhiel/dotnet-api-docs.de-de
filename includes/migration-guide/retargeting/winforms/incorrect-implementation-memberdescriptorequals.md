### <a name="incorrect-implementation-of-memberdescriptorequals"></a><span data-ttu-id="b1ea2-101">Falsche MemberDescriptor.Equals-Implementierung</span><span class="sxs-lookup"><span data-stu-id="b1ea2-101">Incorrect implementation of MemberDescriptor.Equals</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b1ea2-102">Details</span><span class="sxs-lookup"><span data-stu-id="b1ea2-102">Details</span></span>|<span data-ttu-id="b1ea2-103">Ursprüngliche Implementierung der &quot;gleich&quot; Methode wurde zwei verschiedenen Zeichenfolgen-Eigenschaften aus den Objekten unter Vergleich vergleichen: Kategorienamen zu Beschreibungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-103">Original implementation of &quot;Equals&quot; method was comparing two different string properties from the objects under comparison: category name to description string.</span></span> <span data-ttu-id="b1ea2-104">Die Korrektur besteht darin, vergleichen &quot;Kategorie&quot; des ersten Objekts &quot;Kategorie&quot; der zweiten und &quot;Beschreibung&quot; auf &quot;Beschreibung&quot;.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-104">The fix is to compare &quot;category&quot; of first object to &quot;category&quot; of the second one and &quot;description&quot; to &quot;description&quot;.</span></span> <span data-ttu-id="b1ea2-105">Konfigurationswert MemberDescriptorEqualsReturnsFalseIfEquivalent kann festgelegt werden, auf "true", um das neue Verhalten abzuwählen, wenn 4.6.2 Zielobjekte oder auf "false", um diesen Fix zu aktivieren, wenn ansteuern Framework-Version unter 4.6.2 liegt.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-105">MemberDescriptorEqualsReturnsFalseIfEquivalent configuration value can be set to true to opt out of the new behavior if targeting 4.6.2 or to false to enable this fix when targeting framework version is below 4.6.2.</span></span>|
|<span data-ttu-id="b1ea2-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="b1ea2-106">Suggestion</span></span>|<span data-ttu-id="b1ea2-107">MemberDescriptor.Equals manchmal Rückgabe "false" die Anwendung abhängt, wenn Deskriptoren äquivalent sind, und Sie 4.6.2 abzielen Version von .NET Framework gibt es mehrere Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="b1ea2-107">If your application depends on MemberDescriptor.Equals sometimes returning false when descriptors are equivalent, and you are targeting 4.6.2 version of the .NET Framework, you have several options:</span></span><ol><li><span data-ttu-id="b1ea2-108">Stellen Sie die codeänderungen zu vergleichende &quot;Kategorie&quot; und &quot;Beschreibung&quot; Felder manuell neben dem Ausführen von Equals-Methode.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-108">Make code changes to compare &quot;category&quot; and &quot;description&quot; fields manually in addition to running Equals method.</span></span></li><li><span data-ttu-id="b1ea2-109">Keine Teilnahme durch diese Änderung durch den folgenden Wert in der Datei "App.config" hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="b1ea2-109">Opt out from this change by adding the following value to the app.config file:</span></span></li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="b1ea2-110">Wenn Ihre Anwendung Ziele 4.6.1 oder eine niedrigere Version von .NET Framework, und Sie diese Änderung, die aktiviert werden soll, können Sie die Kompatibilitätsschalter auf "false" festlegen, durch den folgenden Wert in der Datei "App.config" hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="b1ea2-110">If your application targets 4.6.1 or lower version of the .NET Framework, and you want this change enabled, you can set the compatibility switch to false by adding the following value to the app.config file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="b1ea2-111">Bereich</span><span class="sxs-lookup"><span data-stu-id="b1ea2-111">Scope</span></span>|<span data-ttu-id="b1ea2-112">Edge</span><span class="sxs-lookup"><span data-stu-id="b1ea2-112">Edge</span></span>|
|<span data-ttu-id="b1ea2-113">Version</span><span class="sxs-lookup"><span data-stu-id="b1ea2-113">Version</span></span>|<span data-ttu-id="b1ea2-114">4.6.2</span><span class="sxs-lookup"><span data-stu-id="b1ea2-114">4.6.2</span></span>|
|<span data-ttu-id="b1ea2-115">Typ</span><span class="sxs-lookup"><span data-stu-id="b1ea2-115">Type</span></span>|<span data-ttu-id="b1ea2-116">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="b1ea2-116">Retargeting</span></span>|
|<span data-ttu-id="b1ea2-117">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="b1ea2-117">Affected APIs</span></span>|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|
