### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>WPF-DispatcherSynchronizationContext.CreateCopy gibt jetzt eine neue Kopie anstelle der aktuellen Instanz zurück.

|   |   |
|---|---|
|Details|In .NET Framework 4 <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> einen Verweis auf die aktuelle Instanz, in erster Linie als zur Optimierung der Leistung zurückgegeben. In .NET Framework 4.5 wird eine neue Instanz zurückgegeben, wodurch es erstmalig möglich ist zu Schlussfolgern, dass gleiche Verweise angeben, dass sich der ausführende Thread im richtigen Synchronisierungskontext befindet.  Es ist unwahrscheinlich, dass Code, der die Identität dieser Verweise überprüft davon betroffen sein sollen, aber aufgrund der Änderung code, Aufrufe <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> sollte im Rahmen der Migration auf .NET Framework 4.5 oder höher getestet werden.|
|Vorschlag|Beachten Sie, <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> wird nun ein neues zurückgeben <xref:System.Threading.SynchronizationContext?displayProperty=name> Objekt. Zuvor wurde Code, der die Gleichheit von Verweisen verwendete, die auf diese Weise generiert wurden, tatsächlich nicht dahingehend überprüft, ob er sich im richtigen Kontext befunden hat. Dies wird jetzt jedoch durchgeführt, wenn bei der Erstellung .NET 4.5 oder höher verwendet wird.  Obwohl es unwahrscheinlich ist, dass dies zu Problemen führt, sollte das Anwenden der betroffenen Codepfade ausreichend sein, um zu ermitteln, ob dies zu Problemen führen kann.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

