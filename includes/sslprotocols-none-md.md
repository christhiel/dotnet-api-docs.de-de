---
ms.openlocfilehash: 733bfb4740f3f274ba9ebb396749d313907d5fa6
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2019
ms.locfileid: "63870374"
---
<span data-ttu-id="a825a-101">Ab .NET Framework 4.7 authentifiziert diese Methode sich mithilfe von <xref:System.Security.Authentication.SslProtocols.None>, was dem Betriebssystem ermöglicht, das am besten geeignete Protokoll auszuwählen und unsichere Protokolle zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="a825a-101">Starting with .NET Framework 4.7, this method authenticates using <xref:System.Security.Authentication.SslProtocols.None>, which allows the operating system to choose the best protocol to use, and to block protocols that are not secure.</span></span> <span data-ttu-id="a825a-102">In .NET Framework 4.6 (und .NET Framework 4.5 mit den neuesten installierten Sicherheitspatches) sind die zulässigen Versionen der TLS/SSL-Protokolle 1.2, 1.1 und 1.0 (es sei denn, Sie deaktivieren die starke Kryptographie durch Bearbeiten der Windows-Registrierung).</span><span class="sxs-lookup"><span data-stu-id="a825a-102">In .NET Framework 4.6 (and .NET Framework 4.5 with the latest security patches installed), the allowed TLS/SSL protocols versions are 1.2, 1.1, and 1.0 (unless you disable strong cryptography by editing the Windows Registry).</span></span>
