### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task nicht mehr "ObjectDisposedException" auslösen, nachdem das Objekt verworfen wurde.

|   |   |
|---|---|
|Details|Mit Ausnahme von <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> mehr Methoden lösen eine <xref:System.ObjectDisposedException?displayProperty=name> Ausnahme aus, nachdem das Objekt freigegeben wurde. Diese Änderung unterstützt die Verwendung von zwischengespeicherten Aufgaben. Beispielsweise kann eine Methode eine zwischengespeicherte Aufgabe zurückgeben, um einen bereits abgeschlossenen Vorgang darzustellen, anstatt eine neue Aufgabe zuzuordnen. Dies war in früheren .NET Framework-Versionen nicht möglich, da jeder Consumer der Aufgabe diese freigeben konnte und somit unbrauchbar machte.|
|Vorschlag|Beachten Sie, dass Task Methoden nicht mehr lösen möglicherweise <xref:System.ObjectDisposedException?displayProperty=name> in Fällen, wenn das Objekt verworfen wird. Wenn eine app je nach wurde diese Ausnahme zu wissen, dass eine Aufgabe freigegeben wurde und es muss aktualisiert werden, um explizit überprüfen Sie den Status der Aufgabe mit <xref:System.Threading.Tasks.Task.Status>.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|

