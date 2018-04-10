### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>Mehrzeilige ASP.Net Textfeld Abstand geändert, wenn AntiXSSEncoder verwenden

|   |   |
|---|---|
|Details|In .NET Framework 4.0 wurden zwischen Zeilen eines mehrzeiligen Textfelds beim Postback zusätzliche Zeilen eingefügt, wenn <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name> verwendet wird. In .NET Framework 4.5 sind diese zusätzlichen Zeilenumbrüche nicht enthalten, wenn die Web-App auf .NET 4.5 ausgerichtet ist.|
|Vorschlag|Beachten Sie, dass bei Web-Apps der Version 4.0, die auf .NET 4.5 neu ausgerichtet wurden, mehrzeilige Textfelder möglicherweise verbessert wurden, damit diese keine zusätzlichen Zeilenumbrüche mehr einfügen. Wenn dies nicht erwünscht ist, kann die app, das alte Verhalten bei der auf .NET Framework 4.5 ausgeführt werden, indem Sie als Ziel .NET Framework 4.0 erforderlich.|
|Bereich|Gering|
|Version|4.5|
|Typ|Neuzuweisung|

