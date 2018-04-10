### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>Mit ClickOnce veröffentlichte Apps, die ein SHA-256-Codesignaturzertifikat verwenden möglicherweise ein auf Windows 2003

|   |   |
|---|---|
|Details|Die ausführbare Datei ist mit SHA256 signiert. Früher wurde sie mit SHA1 signiert, unabhängig davon, ob das Codesignaturzertifikat SHA-1 oder SHA-256 war. Dies gilt für:<ul><li>Alle Anwendungen, die mit Visual Studio 2012 oder höher erstellt wurden.</li><li>Anwendungen, die mit Visual Studio 2010 oder früher auf Systemen mit vorhandenem .NET Framework 4.5 erstellt wurden.</li></ul>Darüber hinaus wird das ClickOnce-Manifest, wenn .NET Framework 4.5 oder höher vorhanden ist, auch mit SHA-256 für SHA-256-Zertifikate signiert, unabhängig von der .NET Framework-Version, mit der es kompiliert wurde.|
|Vorschlag|Die Änderung bei der Signierung der ausführbaren ClickOnce betrifft nur Windows Server 2003-Systeme. Sie müssen KB 938397 installiert werden. Die Änderung bei der Signierung des Manifests mit SHA-256, selbst wenn eine app die .NET Framework 4.0 oder frühere Versionen abzielt, führt eine laufzeitabhängigkeit von .NET Framework 4.5 oder höher.|
|Bereich|Edge|
|Version|4.5|
|Typ|Neuzuweisung|

