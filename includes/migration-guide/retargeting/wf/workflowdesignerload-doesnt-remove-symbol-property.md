### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load symboleigenschafts nicht entfernt werden.

|   |   |
|---|---|
|Details|Wenn im Workflow-Designer, und Laden ein 3.5 neu gehosteten Workflow mit .NET Framework 4.5 abzielt die <xref:System.Activities.Presentation.WorkflowDesigner.Load> -Methode, eine <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> beim Speichern des Workflows ausgelöst wird.|
|Vorschlag|Dieser Fehler nur Manifeste, beim Abzielen auf .NET Framework 4.5 im Workflow-Designer, damit sie hierfür nicht umgangen werden kann die <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> auf die 4.0 .NET Framework.Alternatively das Problem vermieden werden kann, mit der <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> -Methode zum Laden des Workflows anstelle von <xref:System.Activities.Presentation.WorkflowDesigner.Load>.|
|Bereich|Hauptversion|
|Version|4.5|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

