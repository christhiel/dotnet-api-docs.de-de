### <a name="improved-accessibility-for-some-net-sdk-tools"></a>Verbesserte Barrierefreiheit für einige .NET SDK-tools

|   |   |
|---|---|
|Details|In .NET Framework SDK 4.7.1 wurde svcconfigedit.exe und svctraceviewer.exe-Tools verbessert, indem Sie Zugriff auf verschiedene Probleme beheben. Bei den meisten gab kleine Probleme wie z. B. einen nicht definierten Namen oder bestimmte UI-Automatisierung-Muster nicht ordnungsgemäß implementiert wurde. Während viele Benutzer kennen diese falsche Werte wäre, findet Kunden hilfstechnologien wie Sprachausgabe verwenden diese SDK-Tools benutzerfreundlicheren. Sicherlich, ändern Sie diese Hotfixes vorherigen Verhalten, z. B. Tastatur Fokus Reihenfolge. Um alle zu erhalten, die der Zugriff auf diese Tools behebt, können Sie Folgendes in die Datei "App.config":<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Bereich|Edge|
|Version|4.7.1|
|Typ|Neuzuweisung|

