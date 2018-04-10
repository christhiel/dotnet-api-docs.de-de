### <a name="aspnet-mvc-now-escapes-spaces-in-strings-passed-in-via-route-parameters"></a>ASP.NET MVC schützt jetzt Leerzeichen in Zeichenfolgen, die über die Routenparameter übergeben

|   |   |
|---|---|
|Details|Um RFC 2396 zu entsprechen, werden Leerzeichen in Routenpfaden jetzt beim Auffüllen der Aktionsparameter von einer Route mit Escapezeichen versehen. Während <code>/controller/action/some data</code> zuvor mit der Route <code>/controller/action/{data}</code> übereinstimmte und <code>some data</code> als Datenparameter bereitgestellt wurde, stellt sie daher jetzt <code>some%20data</code> bereit.|
|Vorschlag|Der Code sollte aktualisiert werden, um die Escapezeichen der Zeichenfolgenparameter von einer Route zu entfernen. Wenn die ursprüngliche URI benötigt wird, zugegriffen werden kann mit der <xref:System.Net.HttpWebRequest.RequestUri>. OriginalString API.|
|Bereich|Gering|
|Version|4.5.2|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Web.Mvc.RouteAttribute.%23ctor(System.String)?displayProperty=nameWithType></li></ul>|

