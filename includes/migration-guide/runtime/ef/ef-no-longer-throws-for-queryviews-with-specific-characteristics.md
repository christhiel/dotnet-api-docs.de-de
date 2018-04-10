### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>EF löst nicht mehr für Abfrageansichten mit bestimmten Merkmalen

|   |   |
|---|---|
|Details|Entity Framework löst keine mehr aus einer <xref:System.StackOverflowException?displayProperty=name> -Ausnahme aus, wenn eine app eine Abfrage ausführt, die umfasst eine QueryView eine 0.. 1 Navigationseigenschaft, die versucht, die verwandten Entitäten als Teil der Abfrage zu verwenden. Z. B. durch Aufrufen von <code>.Include(e =&gt; e.RelatedNavProp)</code>.|
|Vorschlag|Diese Änderung betrifft nur Code, der Abfrageansichten mit 1-0.. 1 Beziehungen Abfragen ausführt, von denen aufgerufen. Enthalten. Diese Änderung verbessert die Zuverlässigkeit und sollte für beinahe alle Apps transparent sein. Falls jedoch ein unerwünschtes Verhalten auftritt, können Sie dieses Feature deaktivieren, indem Sie den folgenden Eintrag im <code>&lt;appSettings&gt;</code>-Bereich der Anwendungskonfigurationsdatei einfügen:<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.5.2|
|Typ|Laufzeit|

