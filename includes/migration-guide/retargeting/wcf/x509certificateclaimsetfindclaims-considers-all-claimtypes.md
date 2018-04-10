### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims berücksichtigt alle claimTypes

|   |   |
|---|---|
|Details|In apps, .NET Framework 4.6.1, ausgerichtet Anspruchssatz über ein Zertifikat mit mehreren DNS-Einträge in seinem SAN-Feld initialisiert wird, wenn ein X509, die <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> Methode versucht, mit dem Argument ClaimType mit allen DNS-Einträgen überein. Für apps, die auf frühere Versionen von .NET Framework abzielen die <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> Methode versucht, das Argument ClaimType nur mit den letzten DNS-Eintrag entspricht.|
|Vorschlag|Diese Änderung wirkt sich nur auf Anwendungen aus, die auf .NET Framework 4.6.1 ausgerichtet sind. Diese Änderung kann mit dem [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation)-Kompatibilitätsschalter deaktiviert werden (oder aktiviert, bei der Ausrichtung auf Versionen vor 4.6.1).|
|Bereich|Gering|
|Version|4.6.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

