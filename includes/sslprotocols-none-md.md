---
ms.openlocfilehash: 733bfb4740f3f274ba9ebb396749d313907d5fa6
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2019
ms.locfileid: "63870374"
---
Ab .NET Framework 4.7 authentifiziert diese Methode sich mithilfe von <xref:System.Security.Authentication.SslProtocols.None>, was dem Betriebssystem ermöglicht, das am besten geeignete Protokoll auszuwählen und unsichere Protokolle zu blockieren. In .NET Framework 4.6 (und .NET Framework 4.5 mit den neuesten installierten Sicherheitspatches) sind die zulässigen Versionen der TLS/SSL-Protokolle 1.2, 1.1 und 1.0 (es sei denn, Sie deaktivieren die starke Kryptographie durch Bearbeiten der Windows-Registrierung).
