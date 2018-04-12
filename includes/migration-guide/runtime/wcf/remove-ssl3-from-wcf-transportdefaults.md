### <a name="remove-ssl3-from-the-wcf-transportdefaults"></a><span data-ttu-id="ab95e-101">Der WCF-TransportDefaults Ssl3 aufheben</span><span class="sxs-lookup"><span data-stu-id="ab95e-101">Remove Ssl3 from the WCF TransportDefaults</span></span>

|   |   |
|---|---|
|<span data-ttu-id="ab95e-102">Details</span><span class="sxs-lookup"><span data-stu-id="ab95e-102">Details</span></span>|<span data-ttu-id="ab95e-103">Bei der Verwendung von NetTcp im Transportsicherheitsmodus und der Einstellung „Zertifikat“ wird das SSL3-Protokoll nicht mehr als eins der Standardprotokolle für das Aushandeln einer sicheren Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab95e-103">When using NetTcp with transport security and a credential type of certificate, the SSL 3 protocol is no longer a default protocol used for negotiating a secure connection.</span></span> <span data-ttu-id="ab95e-104">In den meisten Fällen darf es keine Auswirkungen auf vorhandene apps wie TLS 1.0 für NetTcp immer in der Protokollliste eingeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ab95e-104">In most cases there should be no impact to existing apps as TLS 1.0 has always been included in the protocol list for NetTcp.</span></span> <span data-ttu-id="ab95e-105">Alle vorhandenen Clients sollten in der Lage sein, eine Verbindung mit mindestens TLS 1.0 auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="ab95e-105">All existing clients should be able to negotiate a connection using at least TLS1.0.</span></span>|
|<span data-ttu-id="ab95e-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="ab95e-106">Suggestion</span></span>|<span data-ttu-id="ab95e-107">Wenn Ssl3 erforderlich ist, verwenden Sie eine der folgenden Konfigurationsmechanismen, die Ssl3 zur Liste der ausgehandelte Protokolle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ab95e-107">If Ssl3 is required, use one of the following configuration mechanisms to add Ssl3 to the list of negotiated protocols.</span></span><ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols></li><li>[<](~/docs/framework/configure-apps/file-schema/wcf/transport-of-nettcpbinding.md)</li><li><span data-ttu-id="ab95e-108">[&lt;sslStreamSecurity&gt; section of &lt;customBinding&gt;]~/docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="ab95e-108">[&lt;sslStreamSecurity&gt; section of &lt;customBinding&gt;]~/docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)</span></span></li></ul>|
|<span data-ttu-id="ab95e-109">Bereich</span><span class="sxs-lookup"><span data-stu-id="ab95e-109">Scope</span></span>|<span data-ttu-id="ab95e-110">Edge</span><span class="sxs-lookup"><span data-stu-id="ab95e-110">Edge</span></span>|
|<span data-ttu-id="ab95e-111">Version</span><span class="sxs-lookup"><span data-stu-id="ab95e-111">Version</span></span>|<span data-ttu-id="ab95e-112">4.6.2</span><span class="sxs-lookup"><span data-stu-id="ab95e-112">4.6.2</span></span>|
|<span data-ttu-id="ab95e-113">Typ</span><span class="sxs-lookup"><span data-stu-id="ab95e-113">Type</span></span>|<span data-ttu-id="ab95e-114">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="ab95e-114">Runtime</span></span>|
|<span data-ttu-id="ab95e-115">Betroffene APIs</span><span class="sxs-lookup"><span data-stu-id="ab95e-115">Affected APIs</span></span>|<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols?displayProperty=nameWithType></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols?displayProperty=nameWithType></li></ul>|
