### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash gibt "false" jetzt für alle Verifizierungsfehler

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.6.2, Rückgabe dieser Methode <strong>"false"</strong> , wenn die Signatur selbst falsch formatiert ist. Es gibt jetzt für alle Fehler bei der computerüberprüfung "false" zurück. In .NET Framework 4.6 und 4.6.1, löst die Methode eine <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> , wenn die Signatur selbst falsch formatiert ist.|
|Vorschlag|Jeglicher Code, dessen Ausführung abhängig, auf die Behandlung ist, der <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> sollten stattdessen ausgeführt werden, wenn die Validierung fehlschlägt und die Methode gibt <strong>"false"</strong>.|
|Bereich|Gering|
|Version|4.6.2|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

