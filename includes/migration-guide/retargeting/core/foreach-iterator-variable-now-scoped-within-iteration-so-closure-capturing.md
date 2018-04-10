### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Foreach Iteratorvariable wurde innerhalb der Iteration Bereich zugewiesen. daher erfassen Closure-Semantik (in C# 5) unterschiedlich sind.

|   |   |
|---|---|
|Details|Beginnend mit C#-5 (Visual Studio 2012) <code>foreach</code> Iteratorvariablen beziehen sich in der Iteration. Dadurch kann unterbrochen, wenn Code die Variablen nicht im einzuschließenden zuvor abhängig war die <code>foreach</code>Schließung des. Das Symptom dieser Änderung ist, dass eine Iteratorvariable an einen Delegaten übergeben behandelt wird, da der Wert, der zum Zeitpunkt der Delegat hat, statt des Werts erstellt wird, die sie zu dem Zeitpunkt, wenn der Delegat aufgerufen wird.|
|Vorschlag|Idealerweise sollte der Code aktualisiert werden, um das neue Compilerverhalten zu erwarten. Wenn die alte Semantik erforderlich ist, kann die Iteratorvariable durch eine separate Variable ersetzt werden, die explizit außerhalb des Gültigkeitsbereichs der Schleife platziert wird.|
|Bereich|Hauptversion|
|Version|4.5|
|Typ|Neuzuweisung|

