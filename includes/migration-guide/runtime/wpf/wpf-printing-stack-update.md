### <a name="wpf-printing-stack-update"></a>WPF-drucken-Stack-Update

|   |   |
|---|---|
|Details|Der WPF drucken-APIs verwenden <xref:System.Printing.PrintQueue?displayProperty=name> jetzt Fensters drucken Dokument Paket-API, zugunsten der jetzt als veraltet markierte XPS-drucken-API aufrufen. Die Änderung vorgenommen wurde mit Wartungsfreundlichkeit Bedenken; Alle Änderungen im Verhalten oder die API-Nutzung sollten Benutzer weder Entwickler angezeigt werden. Der neue Stapel Drucken ist standardmäßig aktiviert, bei der Ausführung in Windows 10-Ersteller-Update. Die alte drucken Stapel wird weiterhin wie zuvor in älteren Versionen von Windows funktionieren weiterhin.|
|Vorschlag|Um den alten Stapel in Windows 10-Ersteller-Update verwenden möchten, legen die <code>UseXpsOMPrinting</code> REG_DWORD-Wert, der die <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> Registrierungsschlüssel <code>1</code>.|
|Bereich|Edge|
|Version|4.7|
|Typ|Laufzeit|

