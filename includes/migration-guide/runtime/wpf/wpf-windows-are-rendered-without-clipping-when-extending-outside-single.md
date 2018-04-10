### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>WPF-Fenster werden ohne Clipping gerendert, wenn außerhalb eines einzelnen Monitors erweitern

|   |   |
|---|---|
|Details|In der .NET Framework 4.6 ausgeführt wird, auf Windows 8 und höher, wird das gesamte Fenster ohne Clipping gerendert, wenn es außerhalb einer einzelnen Anzeige in einem Szenario mit mehreren Monitoren erweitert. Dies unterscheidet sich von früheren Versionen von .NET Framework die WPF-Fenster clip würde, die über eine einzelne Anzeige erweitert.|
|Vorschlag|Dieses Verhalten (entweder ausgeschnitten oder nicht) kann explizit mithilfe von festgelegt werden die <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> Element im <code>&lt;appSettings&gt;</code> in einer Anwendungskonfigurationsdatei oder durch Festlegen der <code>EnableMultiMonitorDisplayClipping</code> Eigenschaft beim Starten der app.|
|Bereich|Gering|
|Version|4.6|
|Typ|Laufzeit|

