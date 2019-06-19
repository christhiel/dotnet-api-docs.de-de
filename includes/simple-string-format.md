---
ms.openlocfilehash: 483f2c83f4d55aad694ba713c787972178b19e5e
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2019
ms.locfileid: "63872451"
---

Wenn jedoch die **String.Format**-Methode aufgerufen wird, müssen Sie sich nicht auf die genaue Überladung konzentrieren, die Sie aufrufen möchten. Stattdessen können Sie die Methode mit einer [kombinierten Formatzeichenfolge](~/docs/standard/base-types/composite-formatting.md) aufrufen, die mindestens ein Formatelement enthält. Weisen Sie jedem Formatelement einen numerischen Index zu. Der erste Index startet bei 0 (null). Neben dem ersten Zeichenfolgenwert sollte Ihr Methodenaufruf über gleich viele zusätzliche Argumente und Indexwerte verfügen. Beispielsweise sollte eine Zeichenfolge, deren Formatelemente die Indizes 0 und 1 aufweisen, über zwei Argumente verfügen. Dabei sollte ein Argument über bis zu fünf Indizes und eins über sechs Argumente verfügen. Ihr Sprachcompiler ruft dann einen Methodenaufruf einer bestimmten Überladung der **String.Format**-Methode auf.   
 
Weitere Informationen zur **String.Format**-Methode finden Sie unter [Getting started with the String.Format method (Erste Schritte mit der String.Format-Methode)](#Starting) und [Which method do I call? (Welche Methode soll ich aufrufen?)](#FTaskList).    
