### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridViews bei AllowCustomPaging auf "true" festgelegt ist möglicherweise das Ereignis PageIndexChanging beim Verlassen der letzten Seite der Sicht ausgelöst.

|   |   |
|---|---|
|Details|Bewirkt, dass ein Fehler in .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> in einigen Fällen nicht für die Auslösung <xref:System.Web.UI.WebControls.GridView?displayProperty=name>e, die aktiviert haben <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Vorschlag|Dieses Problem behoben wurde in .NET Framework 4.6 und kann durch ein Upgrade auf diese Version von .NET Framework adressiert werden. Als Problem zu umgehen, kann die app führen Sie eine explizite BindGrid für ein beliebiges <code>Page_Load</code> würde, die diese Bedingung erreicht (der <xref:System.Web.UI.WebControls.GridView?displayProperty=name> ist in der letzten Seite und die letzte<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> unterscheidet sich vom <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). Alternativ kann die app so geändert werden Paging (anstelle von benutzerdefinierten Paging), können wie in diesem Szenario nicht das Problem zeigen.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

