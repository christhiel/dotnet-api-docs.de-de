### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs werden wird vom Profiler nicht aufgezählt.

|   |   |
|---|---|
|Details|In der .NET Framework 4.5.1, die die profilerstellungs-API <code>RootReferences2()</code> nie falsch zurückgeben <code>COR_PRF_GC_ROOT_HANDLE</code> (sie werden zurückgegeben, als <code>COR_PRF_GC_ROOT_OTHER</code> stattdessen). Dieses Problem wurde behoben in .NET Framework 4.6 ab.|
|Vorschlag|Dieses Problem behoben wurde in .NET Framework 4.6 und kann durch ein Upgrade auf diese Version von .NET Framework adressiert werden.|
|Bereich|Gering|
|Version|4.5.1|
|Typ|Laufzeit|

