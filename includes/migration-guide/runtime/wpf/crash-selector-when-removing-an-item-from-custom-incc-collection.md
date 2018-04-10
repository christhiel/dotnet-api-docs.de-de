### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>Im Selektor stürzt ab, wenn ein Element aus einer benutzerdefinierten CCE-Auflistung entfernen

|   |   |
|---|---|
|Details|Ein <code>T:System.InvalidOperationException</code> ist möglich, in das folgende Szenario:<ul><li>Die ItemsSource für eine <code>T:System.Windows.Controls.Primitives.Selector</code> ist eine Sammlung durch eine benutzerdefinierte Implementierung von <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>.</li><li>Das ausgewählte Element wird aus der Auflistung entfernt.</li><li>Die <code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> hat <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> =-1 (d. h. einer unbekannten Position).</li></ul>Die Ausnahme Callstack beginnt System.Windows.Threading.Dispatcher.VerifyAccess() am System.Windows.DependencyObject.GetValue (DependencyProperty dp) am System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject -Element) diese Ausnahme kann in .net 4.5 auftreten, wenn die Anwendung mehrere Verteilerthread verfügt. In .net 4.7 kann die Ausnahme auch in Anwendungen mit einem einzelnen Verteilerthread auftreten. Das Problem ist in .net 4.7.1 behoben.|
|Vorschlag|Upgrade auf .net 4.7.1.|
|Bereich|Gering|
|Version|4.7|
|Typ|Laufzeit|

