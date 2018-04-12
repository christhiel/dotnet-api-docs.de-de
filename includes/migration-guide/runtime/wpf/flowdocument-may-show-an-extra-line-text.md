### <a name="flowdocument-may-show-an-extra-line-of-text"></a><span data-ttu-id="7b48b-101">FlowDocument möglicherweise eine zusätzliche Textzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7b48b-101">FlowDocument may show an extra line of text</span></span>

|   |   |
|---|---|
|<span data-ttu-id="7b48b-102">Details</span><span class="sxs-lookup"><span data-stu-id="7b48b-102">Details</span></span>|<span data-ttu-id="7b48b-103">In einigen Fällen ein <xref:System.Windows.Documents.FlowDocument> Element wird eine zusätzliche Textzeile angezeigt, bei der Ausführung in .NET Framework 4.5 verglichen, wie es bei Ausführung auf .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="7b48b-103">In some cases, a <xref:System.Windows.Documents.FlowDocument> element will display an extra line of text when running on the .NET Framework 4.5 compared to how it displayed when run on the .NET Framework 4.0.</span></span> <span data-ttu-id="7b48b-104">Es sind keine bekannten Fällen über die Änderung verursacht eine Verschlechterung der Leistung oder unleserlich, weil anzuzeigende Text, aber es kann dazu führen, dass Text angezeigt werden, die zuvor aus weggelassen wurde eine <xref:System.Windows.Documents.FlowDocument>des anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b48b-104">There are no known cases of the change causing any text to be displayed poorly or illegibly, but it could cause text to appear that previously was omitted from a <xref:System.Windows.Documents.FlowDocument>'s view.</span></span>|
|<span data-ttu-id="7b48b-105">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="7b48b-105">Suggestion</span></span>|<span data-ttu-id="7b48b-106">In einigen Fällen kann die Anzeigeelements PageHeight-Eigenschaft nimmt einen die vergangenen Anzahl von Zeilen angezeigt wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="7b48b-106">In some cases, decreasing the display element's PageHeight property by one can restore the previous number of displayed lines.</span></span>|
|<span data-ttu-id="7b48b-107">Bereich</span><span class="sxs-lookup"><span data-stu-id="7b48b-107">Scope</span></span>|<span data-ttu-id="7b48b-108">Edge</span><span class="sxs-lookup"><span data-stu-id="7b48b-108">Edge</span></span>|
|<span data-ttu-id="7b48b-109">Version</span><span class="sxs-lookup"><span data-stu-id="7b48b-109">Version</span></span>|<span data-ttu-id="7b48b-110">4.5</span><span class="sxs-lookup"><span data-stu-id="7b48b-110">4.5</span></span>|
|<span data-ttu-id="7b48b-111">Typ</span><span class="sxs-lookup"><span data-stu-id="7b48b-111">Type</span></span>|<span data-ttu-id="7b48b-112">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="7b48b-112">Runtime</span></span>|
|<span data-ttu-id="7b48b-113">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="7b48b-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|
