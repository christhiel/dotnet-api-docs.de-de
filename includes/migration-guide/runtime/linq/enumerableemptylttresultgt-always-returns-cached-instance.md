### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt; immer gibt zwischengespeicherte Instanz

|   |   |
|---|---|
|Details|Ab .NET 4.5 <xref:System.Linq.Enumerable.Empty%60%601> gibt immer eine zwischengespeicherte interne Instanz <xref:System.Collections.Generic.IEnumerable%601>. Zuvor <xref:System.Linq.Enumerable.Empty%60%601> würde eine leere zwischenspeichern <xref:System.Collections.Generic.IEnumerable%601> zum Zeitpunkt des API-Aufrufs war dies bedeutet, dass unter bestimmten Umständen in der <xref:System.Linq.Enumerable.Empty%60%601> hieß schnell und gleichzeitig andere Instanzen des Typs für die verschiedenen Aufrufe zurückgegeben werden die -API.|
|Vorschlag|Da das vorherige Verhalten nicht deterministisch war, ist es unwahrscheinlich, dass der Code davon abhängig ist. Jedoch für den unwahrscheinlichen Fall, dass leere Enumerables verglichen werden und dabei erwartet wird, dass diese gelegentlich ungleich sind, sollten explizite leere Arrays erstellt werden (<code>new T[0]</code>), anstatt <xref:System.Linq.Enumerable.Empty%60%601> zu verwenden.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

