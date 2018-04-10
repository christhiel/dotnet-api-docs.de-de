### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition DateTimes gibt geringfügig Zeichenfolge zurück.

|   |   |
|---|---|
|Details|Zeichenfolgendarstellungen <xref:System.Net.Mime.ContentDisposition?displayProperty=name>des aktualisiert wurden, 4.6, immer die Stundenkomponente des darstellen ab einem <xref:System.DateTime?displayProperty=name> mit zwei Ziffern. Dies dient zur Einhaltung von [RFC822](http://www.ietf.org/rfc/rfc0822.txt) und [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). Dies bewirkt, dass <xref:System.Net.Mime.ContentDisposition.ToString> in Version 4.6 eine etwas andere Zeichenfolge in Szenarien zurückgibt, bei denen eines der Zeitelemente der Anordnung vor 10:00 Uhr liegt. Beachten Sie, dass ContentDispositions manchmal serialisiert werden, über die sie in Zeichenfolgen, sodass konvertieren <xref:System.Net.Mime.ContentDisposition.ToString> Operationen, Serialisierung oder GetHashCode Aufrufe sollte überprüft werden.|
|Vorschlag|Erwarten Sie nicht, dass die Zeichenfolgendarstellungen von „ContentDispositions“ aus verschiedenen Versionen von .NET Framework ordnungsgemäß miteinander verglichen werden können. Konvertieren Sie die Zeichenfolgen wieder in „ContentDispositions“, sofern möglich, bevor Sie einen Vergleich durchführen.|
|Bereich|Gering|
|Version|4.6|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

