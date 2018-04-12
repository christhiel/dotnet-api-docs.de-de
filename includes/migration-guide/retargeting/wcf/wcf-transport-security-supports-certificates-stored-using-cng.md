### <a name="wcf-transport-security-supports-certificates-stored-using-cng"></a><span data-ttu-id="6eecc-101">Sicherheit für WCF-Transport unterstützt Zertifikate mit CNG gespeichert</span><span class="sxs-lookup"><span data-stu-id="6eecc-101">WCF transport security supports certificates stored using CNG</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6eecc-102">Details</span><span class="sxs-lookup"><span data-stu-id="6eecc-102">Details</span></span>|<span data-ttu-id="6eecc-103">Beginnend mit apps, die auf .NET Framework 4.6.2, unterstützt die WCF-transportsicherheit Zertifikate mithilfe der Windows-Kryptografie-Bibliothek (CNG) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6eecc-103">Starting with apps that target the .NET Framework 4.6.2, WCF transport security supports certificates stored using the Windows Cryptography Library (CNG).</span></span> <span data-ttu-id="6eecc-104">Diese Unterstützung ist auf die Verwendung von Zertifikaten mit einem öffentlichen Schlüssel beschränkt, der über einen Exponent mit einer Länge von nicht mehr als 32 Bit verfügt.</span><span class="sxs-lookup"><span data-stu-id="6eecc-104">This support is limited to certificates with a public key that has an exponent no more than 32 bits in length.</span></span> <span data-ttu-id="6eecc-105">Wenn eine Anwendung .NET Framework 4.6.2 abzielt, ist dieses Feature standardmäßig aktiviert. In früheren Versionen von .NET Framework, der Versuch, X509 Verwenden von Zertifikaten mit einer CSG softwareschlüsselspeicher-Anbieter löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="6eecc-105">When an application targets the .NET Framework 4.6.2, this feature is on by default.In earlier versions of the .NET Framework, the attempt to use X509 certificates with a CSG key storage provider throws an exception.</span></span>|
|<span data-ttu-id="6eecc-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="6eecc-106">Suggestion</span></span>|<span data-ttu-id="6eecc-107">Apps, die für .NET Framework 4.6.1 und früheren jedoch auf .NET Framework 4.6.2 ausgeführt werden können Unterstützung für CNG-Zertifikate aktivieren, indem Sie die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> Abschnitt der Datei "App.config" oder "Web.config":</span><span class="sxs-lookup"><span data-stu-id="6eecc-107">Apps that target the .NET Framework 4.6.1 and earlier but are running on the .NET Framework 4.6.2 can enable support for CNG certificates by adding the following line to the <code>&lt;runtime&gt;</code> section of the app.config or web.config file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableCngCertificates=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="6eecc-108">Dies kann mithilfe des folgenden Codes auch programmgesteuert erfolgen:</span><span class="sxs-lookup"><span data-stu-id="6eecc-108">This can also be done programmatically with the following code:</span></span><pre><code class="language-cs">private const string DisableCngCertificates = @&quot;Switch.System.ServiceModel.DisableCngCertificate&quot;;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, false);&#13;&#10;</code></pre><pre><code class="language-vb">Const DisableCngCertificates As String = &quot;Switch.System.ServiceModel.DisableCngCertificates&quot;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, False)&#13;&#10;</code></pre><span data-ttu-id="6eecc-109">Beachten Sie, dass aufgrund dieser Änderung jeglicher Code zur Ausnahmebehandlung, der von dem Versuch zur Einleitung von sicherer Kommunikation mit einem CNG-Zertifikat abhängt, nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6eecc-109">Note that, because of this change, any exception handling code that depends on the attempt to initiate secure communication with a CNG certificate to fail will no longer execute.</span></span>|
|<span data-ttu-id="6eecc-110">Bereich</span><span class="sxs-lookup"><span data-stu-id="6eecc-110">Scope</span></span>|<span data-ttu-id="6eecc-111">Gering</span><span class="sxs-lookup"><span data-stu-id="6eecc-111">Minor</span></span>|
|<span data-ttu-id="6eecc-112">Version</span><span class="sxs-lookup"><span data-stu-id="6eecc-112">Version</span></span>|<span data-ttu-id="6eecc-113">4.6.2</span><span class="sxs-lookup"><span data-stu-id="6eecc-113">4.6.2</span></span>|
|<span data-ttu-id="6eecc-114">Typ</span><span class="sxs-lookup"><span data-stu-id="6eecc-114">Type</span></span>|<span data-ttu-id="6eecc-115">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="6eecc-115">Retargeting</span></span>|
