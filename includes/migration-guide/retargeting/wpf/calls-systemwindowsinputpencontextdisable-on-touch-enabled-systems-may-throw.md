### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Aufrufe von System.Windows.Input.PenContext.Disable auf touchfähigem Systemen möglicherweise ArgumentException ausgelöst.

|   |   |
|---|---|
|Details|Unter bestimmten Umständen aufgerufen, mit dem internen <strong>System.Windows.Intput.PenContext.Disable</strong> Methode auf touchfähigem Systemen kann ein nicht behandeltes auslösen <code>T:System.ArgumentException</code> aufgrund erneutes eintreten.|
|Vorschlag|Dieses Problem wurde in der .NET Framework-4.7 behoben. Um die Ausnahme zu vermeiden, aktualisieren Sie auf eine Version von .NET Framework mit der .NET Framework-4.7 ab.|
|Bereich|Edge|
|Version|4.6.1|
|Typ|Neuzuweisung|

