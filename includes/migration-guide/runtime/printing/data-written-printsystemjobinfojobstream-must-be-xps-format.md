### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>In PrintSystemJobInfo.JobStream geschriebene Daten müssen im XPS-Format vorliegen.

|   |   |
|---|---|
|Details|Die <xref:System.Printing.PrintSystemJobInfo.JobStream> -Eigenschaft macht den Datenstrom eines Druckauftrags verfügbar. Der Benutzer kann unformatierte Daten an den zugrunde liegenden Betriebssystem Druckkomponenten per in diesen Datenstrom geschrieben. Beginnend mit .NET Framework 4.5 auf Windows 8 und höheren Versionen von Windows-Betriebssystems, müssen in diesen Datenstrom geschriebene Daten als Paketdatenstrom im XPS-Format sein.|
|Vorschlag|Zum Ausgeben der Druckinhalte können Sie einen der folgenden Schritte ausführen:<ul><li>Verwenden Sie die <xref:System.Windows.Xps.XpsDocumentWriter>-Klasse, um Druckinhalte auszugeben. Dies ist die empfohlene Alternative.</li><li>Stellen Sie sicher, dass die Daten an den von zurückgegebenen Datenstrom gesendet die <xref:System.Printing.PrintSystemJobInfo.JobStream> Eigenschaft befindet sich im XPS-Format als Paketdatenstrom vorliegen.</li></ul>|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

