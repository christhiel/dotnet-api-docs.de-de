Mithilfe der Indizierung zeichenbasierte, mit der <xref:System.Text.StringBuilder.Chars%2A> Eigenschaft kann in den folgenden Situationen extrem langsam sein:

- Die <xref:System.Text.StringBuilder> Instanz groß ist (z. B. besteht aus mehreren Zehntausenden von Zeichen).
- Die <xref:System.Text.StringBuilder> ist "segmentierte". Wiederholte Aufrufe von Methoden wie z. B. <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> haben automatisch erweitert, des Objekts <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> Eigenschaft und jedes zugeordnete neue Blöcke von Arbeitsspeicher zu.

Da jedes Zeichen Zugriff die gesamte verknüpfte Liste von Ausschnitten, um die richtige Puffergröße zu indizierenden in Suchen führt, wird die Leistung erheblich beeinträchtigt.

> [!NOTE]
>  Dies gilt auch für eine große "segmentierte" <xref:System.Text.StringBuilder> -Objekt unter Verwendung der <xref:System.Text.StringBuilder.Chars%2A> -Eigenschaft für Index-basierten Zugriff auf eine oder eine kleine Anzahl von Zeichen hat Auswirkungen auf die Leistung unerheblich; in der Regel ist ein **0(n)** Vorgang. Die erheblichen Leistungseinbußen tritt auf, wenn es sich bei die Zeichen in einem durchlaufenden der <xref:System.Text.StringBuilder> Objekt, das eine **O(n^2)** Vorgang. 

Wenn Leistungsprobleme auftreten, bei Verwendung mit Indizierung zeichenbasierte <xref:System.Text.StringBuilder> Objekte aufweist, können Sie jede der folgenden problemumgehungen verwenden:

- Konvertieren der <xref:System.Text.StringBuilder> -Instanz, auf eine <xref:System.String> durch Aufrufen der <xref:System.Text.StringBuilder.ToString%2A> -Methode, klicken Sie dann Zugriff auf die Zeichen in der Zeichenfolge.

- Kopieren Sie den Inhalt des vorhandenen <xref:System.Text.StringBuilder> Objekt auf eine neue vorab Größe <xref:System.Text.StringBuilder> Objekt. Verbessert die Leistung, da die neue <xref:System.Text.StringBuilder> Objekt ist kein segmentierten. Zum Beispiel:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Legen Sie die anfängliche Kapazität der <xref:System.Text.StringBuilder> Objekt auf einen Wert, der die maximale erwartete Größe ungefähr gleich durch Aufrufen der <xref:System.Text.StringBuilder.%23ctor(System.Int32)> Konstruktor. Beachten Sie, dass dies den gesamten Block Arbeitsspeicher zurück, sogar wenn ordnet die <xref:System.Text.StringBuilder> selten die maximale Kapazität erreicht.
