---
ms.openlocfilehash: c28e3f97e02079905d591a7f27dc8d68d603c0bf
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2019
ms.locfileid: "63871561"
---
<span data-ttu-id="d11c7-101">Der umgekehrte Schrägstrich \\ stellt in Mutex-Namen ein reserviertes Zeichen dar.</span><span class="sxs-lookup"><span data-stu-id="d11c7-101">The backslash (\\) is a reserved character in a mutex name.</span></span> <span data-ttu-id="d11c7-102">Verwenden Sie umgekehrte Schrägstriche (\\) in Mutex-Namen nur wie in dem Hinweis zur Verwendung von Mutex-Objekten in Sitzungen des Terminalservers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d11c7-102">Don't use a backslash (\\) in a mutex name except as specified in the note on using mutexes in terminal server sessions.</span></span> <span data-ttu-id="d11c7-103">Andernfalls kann sogar eine <xref:System.IO.DirectoryNotFoundException> ausgelöst werden, wenn der Mutex-Name für eine bereits vorhandene Datei steht.</span><span class="sxs-lookup"><span data-stu-id="d11c7-103">Otherwise, a <xref:System.IO.DirectoryNotFoundException> may be thrown, even though the name of the mutex represents an existing file.</span></span>
