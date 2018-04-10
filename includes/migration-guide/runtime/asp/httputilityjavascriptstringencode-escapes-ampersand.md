### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a>Kaufmännisches und-Zeichen HttpUtility.JavaScriptStringEncode-Escapezeichen

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.5 <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> versieht das kaufmännische und-Zeichen (&amp;) Zeichen.|
|Vorschlag|Wenn Ihre App vom vorherigen Verhalten dieser Methode abhängig ist, können Sie dem [appSettings-Element von ASP.NET](https://msdn.microsoft.com/library/hh975440.aspx) eine „aspnet:JavaScriptDoNotEncodeAmpersand“-Einstellung in der Konfigurationsdatei hinzufügen.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

