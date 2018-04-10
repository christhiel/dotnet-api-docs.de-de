### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Fehlende Zielframeworkmoniker Ergebnisse 4.0 Verhalten

|   |   |
|---|---|
|Details|Anwendungen ohne eine <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> auf der Assembly Ebene automatisch ausgeführt, mit der Semantik der .NET Framework 4.0 (Quirksmodus) angewendet. Um hohe Qualität zu gewährleisten, wird empfohlen, dass alle Binärdateien explizit zugeschrieben werden eine <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> , der angibt, der Version von .NET Framework, die sie mit erstellt wurden. Beachten Sie, dass eine Zielframeworkmoniker in einer Projektdatei mit MSBuild automatisch anwenden bewirkt eine <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Vorschlag|Ein <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> sollte angegeben werden, entweder über das Attribut hinzufügen, direkt auf die Assembly oder durch Angabe eines Zielframeworks in der [Projektdatei oder über Visual Studio-Projekt-Eigenschaften GUI](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Bereich|Hauptversion|
|Version|4.5|
|Typ|Laufzeit|

