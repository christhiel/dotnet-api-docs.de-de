### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>Profilerstellung für ASP.Net MVC 4-apps kann zu schwerwiegenden Fehler im Ausführungsmodul führen.

|   |   |
|---|---|
|Details|Profiler, die mit NGEN/Profile Assemblys profilierten ASP.NET MVC4-Anwendungen beim Start mit einer "Schwerwiegender Modul Ausführungsausnahme" stürzt möglicherweise ab.|
|Vorschlag|Dieses Problem wurde in .NET Framework 4.5.2 behoben. Alternativ kann der Profiler dieses Problem vermeiden, indem Sie angeben <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> in der Ereignismaske.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|

