### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Nicht mehr damit EnableViewStateMac auf "false" festgelegt

|   |   |
|---|---|
|Details|In ASP.NET sind die folgenden Angaben nicht mehr erlaubt: <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> oder <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. Der Nachrichtenauthentifizierungscode (MAC) des Ansichtszustands wird nun für alle Anfragen mit eingebettetem Ansichtszustand erzwungen. Nur apps, die die Eigenschaft EnableViewStateMac explizit, um festlegen <code>false</code> betroffen sind.|
|Vorschlag|EnableViewStateMac muss "true" werden als eingestuft und jegliche resultierenden MAC Fehler aufgelöst werden müssen (wie in beschrieben [in dieser Anleitung](https://support.microsoft.com/kb/2915218), enthält mehrere Auflösungen abhängig von den gegebenheiten MAC-Fehler Ursache).|
|Bereich|Hauptversion|
|Version|4.5.2|
|Typ|Laufzeit|

