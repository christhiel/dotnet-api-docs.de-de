### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>Opt-in Unterbrechung aus verschiedenen 4.5 SQL-Generierung einfacher 4.0 SQL-Generierung wiederherstellen

|   |   |
|---|---|
|Details|Abfragen, die JOIN-Anweisungen erzeugen und enthalten einen Aufruf an eine einschränkungsoperation ohne vorherige OrderBy jetzt mit generieren einfacheres SQL. Nach dem Upgrade auf .NET Framework 4.5, generieren diese Abfragen komplizierteres SQL als in vorherigen Versionen.|
|Vorschlag|Dieses Feature ist standardmäßig deaktiviert. Wenn Entity Framework zusätzliche JOIN-Anweisungen, die Leistungseinbußen verursachen generiert, können Sie diese Funktion aktivieren, indem Sie den folgenden Eintrag zum Hinzufügen der <code>&lt;appSettings&gt;</code> Abschnitt der Anwendungskonfigurationsdatei (app.config):<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|Bereich|Transparent|
|Version|4.5.2|
|Typ|Laufzeit|

