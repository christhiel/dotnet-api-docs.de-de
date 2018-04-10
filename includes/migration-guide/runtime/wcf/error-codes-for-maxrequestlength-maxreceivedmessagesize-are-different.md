### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Fehlercodes für MaxRequestLength oder "MaxReceivedMessageSize" unterscheiden.

|   |   |
|---|---|
|Details|Nachrichten in WCF-Webdiensten in Internet Information Services (IIS) oder ASP.NET Development Server gehostet, die MaxRequestLength (in ASP.NET) überschreiten, oder "MaxReceivedMessageSize" (in WCF) über ein anderer Fehler CodeThe HTTP-Statuscode 400 (Ungültige Anforderung geändert hat ) zum 413 (Anforderungsentität zu groß) und Nachrichten, die die MaxRequestLength oder die Einstellung "MaxReceivedMessageSize" überschreiten Auslösen einer <xref:System.ServiceModel.ProtocolException?displayProperty=name> Ausnahme. Dies gilt auch für Fälle, in denen der Übertragungsmodus gestreamt wird.|
|Vorschlag|Diese Änderung erleichtert das Debuggen in Fällen, in denen die Nachrichtenlänge die von ASP.NET oder WCF zulässigen Begrenzungen überschreitet. Sie müssen Code ändern, die Verarbeitung basierend auf einen HTTP 400-Statuscode ausführt.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|

