### <a name="httprequestcontentencoding-property-prohibits-utf7"></a>HttpRequest.ContentEncoding Eigenschaft verhindert UTF7

|   |   |
|---|---|
|Details|Ab .NET Framework 4.5, UTF-7-Codierung ist nicht zulässig <xref:System.Web.HttpRequest?displayProperty=name>s "stellen. Teilweise treten bei Daten für Anwendungen, die von eingehenden UTF-7-Daten abhängen, Decodierungsprobleme auf.|
|Vorschlag|Im Idealfall sollte Anwendungen aktualisiert werden, um nicht UTF-7-Codierung verwenden <xref:System.Web.HttpRequest?displayProperty=name>s. Alternativ kann das Legacyverhalten mithilfe des <code>aspnet:AllowUtf7RequestContentEncoding</code>-Attributs des [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx)-Elements wiederhergestellt werden.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|

