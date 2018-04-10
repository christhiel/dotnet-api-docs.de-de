### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce unterstützt SHA-256 auf 4.0 als Ziel-apps

|   |   |
|---|---|
|Details|Zuvor eine ClickOnce-Anwendung mit einem Zertifikat mit SHA-256 signiert, müsste .NET 4.5 oder höher vorhanden sein, selbst wenn die app 4.0 zugewiesen. 4.0 dienenden ClickOnce-apps können jetzt auf 4.0, ausführen, auch wenn mit SHA-256 signiert.|
|Vorschlag|Diese Änderung beseitigt diese Abhängigkeit und gestattet die Verwendung SHA-256-Zertifikaten zum Signieren von ClickOnce-apps, die .NET Framework 4 und früheren Versionen als Ziel verwendet werden.|
|Bereich|Gering|
|Version|4.6|
|Typ|Neuzuweisung|

