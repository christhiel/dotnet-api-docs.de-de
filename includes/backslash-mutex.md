---
ms.openlocfilehash: c28e3f97e02079905d591a7f27dc8d68d603c0bf
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2019
ms.locfileid: "63871561"
---
Der umgekehrte Schrägstrich \\ stellt in Mutex-Namen ein reserviertes Zeichen dar. Verwenden Sie umgekehrte Schrägstriche (\\) in Mutex-Namen nur wie in dem Hinweis zur Verwendung von Mutex-Objekten in Sitzungen des Terminalservers beschrieben. Andernfalls kann sogar eine <xref:System.IO.DirectoryNotFoundException> ausgelöst werden, wenn der Mutex-Name für eine bereits vorhandene Datei steht.
