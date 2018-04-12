### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a><span data-ttu-id="b353c-101">System.Uri.IsWellFormedUriString-Methode zurückgibt für relative URIs mit einem Doppelpunkt "Char" im ersten Segment "false"</span><span class="sxs-lookup"><span data-stu-id="b353c-101">System.Uri.IsWellFormedUriString method returns false for relative URIs with a colon char in first segment</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b353c-102">Details</span><span class="sxs-lookup"><span data-stu-id="b353c-102">Details</span></span>|<span data-ttu-id="b353c-103">Ab .NET Framework 4.5 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> behandelt relativen URIs mit einer <code>:</code> in ihren ersten Segment nicht wohlgeformt.</span><span class="sxs-lookup"><span data-stu-id="b353c-103">Beginning with the .NET Framework 4.5, <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> will treat relative URIs with a <code>:</code> in their first segment as not well formed.</span></span> <span data-ttu-id="b353c-104">Dies ist eine Änderung gegenüber <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> Verhalten in .NET Framework 4.0, die an RFC3986 entsprechen vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="b353c-104">This is a change from <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> behavior in the .NET Framework 4.0 that was made to conform to RFC3986.</span></span>|
|<span data-ttu-id="b353c-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="b353c-105">Suggestion</span></span>|<span data-ttu-id="b353c-106">Diese Änderung (z. B. viele weitere URI-Änderungen) wirkt sich nur auf Anwendungen für .NET Framework 4.5 (oder höher) aus.</span><span class="sxs-lookup"><span data-stu-id="b353c-106">This change (like many other URI changes) will only affect applications targeting the .NET Framework 4.5 (or later).</span></span> <span data-ttu-id="b353c-107">Um das alte Verhalten weiterhin verwenden möchten, die app anhand der .NET Framework 4.0 als Ziel.</span><span class="sxs-lookup"><span data-stu-id="b353c-107">To keep using the old behavior, target the app against the .NET Framework 4.0.</span></span> <span data-ttu-id="b353c-108">Scan Alternativ vor dem Aufruf des URIS <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> sucht <code>:</code> Zeichen, die Sie möglicherweise zu Validierungszwecken, entfernen möchten, wenn das alte Verhalten erwünscht ist.</span><span class="sxs-lookup"><span data-stu-id="b353c-108">Alternatively, scan URI's prior to calling <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> looking for <code>:</code> characters that you may want to remove for validation purposes, if the old behavior is desirable.</span></span>|
|<span data-ttu-id="b353c-109">Bereich</span><span class="sxs-lookup"><span data-stu-id="b353c-109">Scope</span></span>|<span data-ttu-id="b353c-110">Gering</span><span class="sxs-lookup"><span data-stu-id="b353c-110">Minor</span></span>|
|<span data-ttu-id="b353c-111">Version</span><span class="sxs-lookup"><span data-stu-id="b353c-111">Version</span></span>|<span data-ttu-id="b353c-112">4.5</span><span class="sxs-lookup"><span data-stu-id="b353c-112">4.5</span></span>|
|<span data-ttu-id="b353c-113">Typ</span><span class="sxs-lookup"><span data-stu-id="b353c-113">Type</span></span>|<span data-ttu-id="b353c-114">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="b353c-114">Retargeting</span></span>|
|<span data-ttu-id="b353c-115">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="b353c-115">Affected APIs</span></span>|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|
