### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage löst nicht mehr für eintrittsinvariante IMessageFilter.PreFilterMessage-Implementierungen

|   |   |
|---|---|
|Details|Vor .NET Framework 4.6.1, Aufrufen <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> mit einer <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> die bezeichnet <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> oder <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (während des Aufrufs auch <xref:System.Windows.Forms.Application.DoEvents>) würde dazu führen, dass ein <xref:System.IndexOutOfRangeException?displayProperty=name>. Beginnend mit Anwendungen, die für .NET Framework 4.6.1, wird diese Ausnahme nicht mehr ausgelöst, und eintrittsinvariante Filter wie oben beschrieben dürfen verwendet werden.|
|Vorschlag|Beachten Sie, <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> löst nicht mehr für die eintrittsinvariante <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> Verhalten oben beschriebenen. Dies betrifft nur Anwendungen für die .NET Framework 4.6.1.Apps als Ziel .NET Framework 4.6.1 können diese Änderung ablehnen (oder mit älteren Frameworks sich, in entscheiden können apps) mithilfe der [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) Kompatibilitätsschalter.|
|Bereich|Edge|
|Version|4.6.1|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

