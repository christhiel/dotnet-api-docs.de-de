### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant oder Contract.Requires<TException> sollten nicht als reine String.IsNullOrEmpty

|   |   |
|---|---|
|Details|Für apps, .NET Framework 4.6.1, ausgerichtet werden, wenn für die invariante Vertrag <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> oder die Vorbedingungsvertrag für <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> Aufrufe der <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> Methode, die Bearbeiter ausgibt compilerwarnung CC1036: &quot;Aufruf Methode erkannt " System.String.IsNullOrWhteSpace(System.String) "ohne [reiner] in der Methode.&quot; Dies ist eine compilerwarnung als einen Compilerfehler.|
|Vorschlag|Dieses Verhalten wurde in [GitHub-Problem Nr. 339](https://github.com/Microsoft/CodeContracts/issues/339) behandelt. Um diese Warnung zu vermeiden, können Sie herunterladen und kompilieren Sie eine aktualisierte Version des Quellcodes für das Tool Codeverträge aus [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md). Informationen zum Herunterladen befinden sich am unteren Rand der Seite.|
|Bereich|Gering|
|Version|4.6.1|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

