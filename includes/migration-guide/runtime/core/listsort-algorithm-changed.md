### <a name="listsort-algorithm-changed"></a>List.Sort-Algorithmus geändert

|   |   |
|---|---|
|Details|Ab .NET Framework 4.5, <xref:System.Collections.Generic.List%601?displayProperty=name>des Sortieralgorithmus wurde geändert, (um eine introspective Sortierung anstelle einer schnellen Sortierung sein). <xref:System.Collections.Generic.List%601?displayProperty=name>die Sortierreihenfolge wurde nie stabil, diese Änderung verursacht jedoch möglicherweise verschiedene Szenarien zum Sortieren in instabilen Möglichkeiten. Das bedeutet einfach, dass entsprechende Elemente in verschiedenen Reihenfolgen bei nachfolgenden Aufrufen der API sortieren können.|
|Vorschlag|Da die alte Sortieralgorithmus war auch (Obwohl in leicht variieren) instabil ist, es darf kein Code, von denen abhängt entsprechende Elemente immer in einer bestimmten Reihenfolge sortieren. Wenn Instanzen des Codes je nach, und wird mit dem alten Verhalten Glück vorhanden sind, sollten diesen Code aktualisiert werden, um eine verwendet werden soll, die deterministisch die Elemente in der gewünschten Reihenfolge sortiert werden sollen.|
|Bereich|Transparent|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

