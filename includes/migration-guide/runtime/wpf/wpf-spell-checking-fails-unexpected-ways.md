### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>WPF-Rechtschreibprüfung auf unerwartete Weise ein Fehler auftritt

|   |   |
|---|---|
|Details|Dies umfasst eine Reihe von WPF-Rechtschreibprüfung Punkten:<ul><li>WPF-Rechtschreibprüfung in einigen Fällen löst aus <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>WPF-Rechtschreibprüfung schlägt mit <xref:System.UnauthorizedAccessException> bei Anwendungen mithilfe von "Ausführen als anderer Benutzer" gestartet werden</li><li>WPF-Rechtschreibprüfung identifiziert falsch Rechtschreibfehler im zusammengesetzte Wörter wie "Hausnummer" auf Deutsch.</li></ul>|
|Vorschlag|Problem #1 – dieser Fehler wurde in .NET Framework 4.6.2 behoben Problem Nr. 2 - WPF-Rechtschreibprüfung wird nicht mehr unterstützt, wenn Anwendungen mithilfe von "Ausführen als anderer Benutzer" gestartet werden. Ab .NET Framework 4.6.2, Anwendungen, die auf diese Weise gestartet werden nicht mehr Anwendungsabstürzen - stattdessen die Rechtschreibprüfung im Hintergrund deaktiviert sein. Problem #3 – dieser Fehler wurde in .NET Framework 4.6.2 behoben.|
|Bereich|Edge|
|Version|4.6.1|
|Typ|Laufzeit|

