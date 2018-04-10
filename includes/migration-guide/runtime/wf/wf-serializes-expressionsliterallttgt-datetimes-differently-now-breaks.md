### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF serialisiert Expressions.Literal&lt;T&gt; datetimes verstrichen ist jetzt anders (benutzerdefinierte XAML-Parser unterbricht)

|   |   |
|---|---|
|Details|Die zugeordnete <xref:System.Windows.Markup.ValueSerializer> -Objekt konvertiert ein <xref:System.DateTime?displayProperty=name> oder <xref:System.DateTimeOffset?displayProperty=name> -Objekt, dessen zweites und <xref:System.DateTime.Millisecond?displayProperty=name> Komponenten sind nicht 0 (null) und (für eine <xref:System.DateTime?displayProperty=name> Wert), dessen <xref:System.DateTime.Kind> Eigenschaft ist nicht auf Property-Element nicht angegeben Die Syntax anstelle einer Zeichenfolge. Durch diese Änderung kann bei <xref:System.DateTime?displayProperty=name>- und <xref:System.DateTimeOffset?displayProperty=name>-Werten ein Roundtrip ausgeführt werden. Benutzerdefinierte XAML-Parser, die davon ausgehen, dass sich Eingabe-XAML in der Attributsyntax befindet, funktionieren nicht ordnungsgemäß.|
|Vorschlag|Durch diese Änderung kann bei <xref:System.DateTime?displayProperty=name>- und <xref:System.DateTimeOffset?displayProperty=name>-Werten ein Roundtrip ausgeführt werden. Benutzerdefinierte XAML-Parser, die davon ausgehen, dass sich Eingabe-XAML in der Attributsyntax befindet, funktionieren nicht ordnungsgemäß.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|

