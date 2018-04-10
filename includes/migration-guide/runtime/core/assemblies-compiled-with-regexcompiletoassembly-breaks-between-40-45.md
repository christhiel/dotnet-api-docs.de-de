### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>Mit Regex.CompileToAssembly Umbrüche zwischen 4.0 und 4.5 kompilierte Assemblys

|   |   |
|---|---|
|Details|Wenn eine Assembly aus kompilierten regulären Ausdrücken mit dem .NET Framework 4.5, aber .NET Framework 4-Ziele erstellt wird, versucht, eine für reguläre Ausdrücke verwenden, da die Assembly auf einem System mit .NET Framework 4 installiert eine Ausnahme ausgelöst.|
|Vorschlag|Um dieses Problem zu umgehen, haben Sie die folgenden Möglichkeiten:<ul><li>Erstellen Sie die Assembly, die die regulären Ausdrücke mit .NET Framework 4 enthält.</li><li>Verwenden Sie einen interpretierten regulären Ausdruck.</li></ul>|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

