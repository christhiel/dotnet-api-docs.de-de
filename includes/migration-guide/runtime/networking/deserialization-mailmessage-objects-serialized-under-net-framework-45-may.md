### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>Deserialisierung von MailMessage-Objekten, die unter .NET Framework 4.5 serialisiert kann fehlschlagen.

|   |   |
|---|---|
|Details|Beginnend mit .NET Framework 4.5 <xref:System.Web.Mail.MailMessage> Objekte können nicht-ASCII-Zeichen enthalten. In .NET Framework 4 werden nur ASCII-Zeichen unterstützt. <xref:System.Web.Mail.MailMessage> Objekte, die nicht-ASCII-Zeichen enthalten und serialisiert sind, klicken Sie unter .NET Framework 4.5 oder höher, können unter .NET Framework 4 nicht deserialisiert werden.|
|Vorschlag|Stellen Sie sicher, dass Ihr Code die Ausnahmebehandlung bietet bei der Deserialisierung ein <xref:System.Web.Mail.MailMessage> Objekt.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

