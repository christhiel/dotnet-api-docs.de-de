### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>System.Uri.IsWellFormedUriString-Methode zurückgibt für relative URIs mit einem Doppelpunkt "Char" im ersten Segment "false"

|   |   |
|---|---|
|Details|Ab .NET Framework 4.5 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> behandelt relativen URIs mit einer <code>:</code> in ihren ersten Segment nicht wohlgeformt. Dies ist eine Änderung gegenüber <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> Verhalten in .NET Framework 4.0, die an RFC3986 entsprechen vorgenommen wurde.|
|Vorschlag|Diese Änderung (z. B. viele weitere URI-Änderungen) wirkt sich nur auf Anwendungen für .NET Framework 4.5 (oder höher) aus. Um das alte Verhalten weiterhin verwenden möchten, die app anhand der .NET Framework 4.0 als Ziel. Scan Alternativ vor dem Aufruf des URIS <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> sucht <code>:</code> Zeichen, die Sie möglicherweise zu Validierungszwecken, entfernen möchten, wenn das alte Verhalten erwünscht ist.|
|Bereich|Gering|
|Version|4.5|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

