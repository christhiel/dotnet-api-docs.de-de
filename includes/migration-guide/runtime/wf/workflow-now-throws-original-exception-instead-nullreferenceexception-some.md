### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Workflow löst jetzt ursprünglichen Ausnahme anstelle von NullReferenceException in einigen Fällen aus.

|   |   |
|---|---|
|Details|In .NET Framework 4.6.2 und früheren Versionen, wenn die Execute-Methode einer Workflow-Aktivität eine Ausnahme mit einer <code>null</code> Wert für die <xref:System.Exception.Message> -Eigenschaft, die Workflowlaufzeit System.Activities löst eine <xref:System.NullReferenceException?displayProperty=name>, Masking der ursprüngliche Ausnahme. In der .NET Framework-4.7 wird die zuvor maskierte Ausnahme ausgelöst.|
|Vorschlag|Wenn Codes Behandlung verwendet die <xref:System.NullReferenceException?displayProperty=name>, ändern Sie ihn zum Abfangen von Ausnahmen, die von Ihren benutzerdefinierten Aktivitäten ausgelöst werden kann.|
|Bereich|Gering|
|Version|4.7|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

