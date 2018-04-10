### <a name="xslt-forward-compat-now-works"></a>XSLT-forward-Compat funktioniert jetzt ordnungsgemäß.

|   |   |
|---|---|
|Details|In .NET Framework 4 verfügte XSLT 1.0-Vorwärtskompatibilität folgende Probleme:<ul><li>Beim Laden eines Stylesheets trat ein Fehler auf, wenn die Version auf 2.0 festgelegt war und der Parser ein unbekanntes XSLT 1.0-Konstrukt feststellte.</li><li>Das <code>xsl:sort</code>-Konstrukt konnte keine Daten sortieren, wenn die Stylesheetversion auf 1.1 festgelegt war.</li></ul>In .NET Framework 4.5 wurden diese Probleme behoben und XSLT 1.0-vorwärtskompatibilitätsmodus funktioniert ordnungsgemäß.|
|Vorschlag|Die meisten apps sollten nicht betroffen, können, jedoch Daten in einigen Fällen nun, dass xsl: Sort Quellfensterinhalts berücksichtigt wird anders sortiert werden. Wenn <code>xsl:sort</code> ist in 1.1 Stylesheets verwendet wird, bestätigen Sie, dass apps die unsortierte Reihenfolge der Daten nicht abhängig sind. Wenn das Sortierverhalten 4.0 apps benötigen, entfernen Sie <code>xsl:sort</code> aus dem Stylesheet.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

