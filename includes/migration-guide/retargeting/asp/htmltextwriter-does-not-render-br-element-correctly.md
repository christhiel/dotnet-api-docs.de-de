### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter rendert nicht `<br/>` Element ordnungsgemäß

|   |   |
|---|---|
|Details|Ab .NET Framework 4.6 fügt der Aufruf von <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> und <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> mit einem <code>&lt;BR /&gt;</code>-Element ordnungsgemäß nur ein (anstatt zwei) <code>&lt;BR /&gt;</code> ein.|
|Vorschlag|Wenn eine App vom zusätzlichen <code>&lt;BR /&gt;</code>-Tag abhängig ist, sollte <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> ein zweites Mal aufgerufen werden. Beachten Sie, dass dieses verhaltensänderung nur apps, die auf .NET Framework 4.6 oder höher abzielen betrifft, damit eine weitere Option eine frühere Version von .NET Framework abzielen ist, um das alte Verhalten zu erzielen.|
|Bereich|Edge|
|Version|4.6|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

