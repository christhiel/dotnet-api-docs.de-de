### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Einige WorkFlow Drag-and-Drop-APIs sind veraltet

|   |   |
|---|---|
|Details|Dieser WorkFlow Drag-and-Drop-API ist veraltet und compilerwarnungen verursacht, wenn die app für 4.5 neu erstellt wird.|
|Vorschlag|Neue <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> APIs, die Vorgänge mit mehreren Objekten unterstützen sollte stattdessen verwendet werden. Alternativ können die Buildwarnungen unterdrückt oder durch die Verwendung eines älteren Compilers vermieden werden. Die APIs werden weiterhin unterstützt.|
|Bereich|Gering|
|Version|4.5|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

