### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>Alle Server in der Webfarm, verwenden Sie die gleiche Version von .NET Framework erfordert Freigeben des Sitzungszustands mit Asp.Net "StateServer"

|   |   |
|---|---|
|Details|Bei der Aktivierung <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> Sitzung aufweist, müssen alle Server in der angegebenen Webfarm die gleiche Version von .NET Framework in der Reihenfolge für den Status verwenden, ordnungsgemäß freigegeben werden.|
|Vorschlag|Achten Sie darauf, dass Sie .NET Framework-Versionen auf Webservern zu aktualisieren, die zur gleichen Zeit ihren Zustand freigeben.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

