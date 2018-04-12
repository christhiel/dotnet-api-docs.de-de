### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a><span data-ttu-id="a884b-101">Foreach Iteratorvariable wurde innerhalb der Iteration Bereich zugewiesen. daher erfassen Closure-Semantik (in C# 5) unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="a884b-101">Foreach iterator variable is now scoped within the iteration, so closure capturing semantics are different (in C#5)</span></span>

|   |   |
|---|---|
|<span data-ttu-id="a884b-102">Details</span><span class="sxs-lookup"><span data-stu-id="a884b-102">Details</span></span>|<span data-ttu-id="a884b-103">Beginnend mit C#-5 (Visual Studio 2012) <code>foreach</code> Iteratorvariablen beziehen sich in der Iteration.</span><span class="sxs-lookup"><span data-stu-id="a884b-103">Beginning with C# 5 (Visual Studio 2012), <code>foreach</code> iterator variables are scoped within the iteration.</span></span> <span data-ttu-id="a884b-104">Dadurch kann unterbrochen, wenn Code die Variablen nicht im einzuschließenden zuvor abhängig war die <code>foreach</code>Schließung des.</span><span class="sxs-lookup"><span data-stu-id="a884b-104">This can cause breaks if code was previously depending on the variables to not be included in the <code>foreach</code>'s closure.</span></span> <span data-ttu-id="a884b-105">Das Symptom dieser Änderung ist, dass eine Iteratorvariable an einen Delegaten übergeben behandelt wird, da der Wert, der zum Zeitpunkt der Delegat hat, statt des Werts erstellt wird, die sie zu dem Zeitpunkt, wenn der Delegat aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a884b-105">The symptom of this change is that an iterator variable passed to a delegate is treated as the value it has at the time the delegate is created, rather than the value it has at the time the delegate is invoked.</span></span>|
|<span data-ttu-id="a884b-106">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="a884b-106">Suggestion</span></span>|<span data-ttu-id="a884b-107">Idealerweise sollte der Code aktualisiert werden, um das neue Compilerverhalten zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="a884b-107">Ideally, code should be updated to expect the new compiler behavior.</span></span> <span data-ttu-id="a884b-108">Wenn die alte Semantik erforderlich ist, kann die Iteratorvariable durch eine separate Variable ersetzt werden, die explizit außerhalb des Gültigkeitsbereichs der Schleife platziert wird.</span><span class="sxs-lookup"><span data-stu-id="a884b-108">If the old semantics are required, the iterator variable can be replaced with a separate variable which is explicitly placed outside of the loop's scope.</span></span>|
|<span data-ttu-id="a884b-109">Bereich</span><span class="sxs-lookup"><span data-stu-id="a884b-109">Scope</span></span>|<span data-ttu-id="a884b-110">Hauptversion</span><span class="sxs-lookup"><span data-stu-id="a884b-110">Major</span></span>|
|<span data-ttu-id="a884b-111">Version</span><span class="sxs-lookup"><span data-stu-id="a884b-111">Version</span></span>|<span data-ttu-id="a884b-112">4.5</span><span class="sxs-lookup"><span data-stu-id="a884b-112">4.5</span></span>|
|<span data-ttu-id="a884b-113">Typ</span><span class="sxs-lookup"><span data-stu-id="a884b-113">Type</span></span>|<span data-ttu-id="a884b-114">Neuzuweisung</span><span class="sxs-lookup"><span data-stu-id="a884b-114">Retargeting</span></span>|
