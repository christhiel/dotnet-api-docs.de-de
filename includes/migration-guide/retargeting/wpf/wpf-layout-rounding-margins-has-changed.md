### <a name="wpf-layout-rounding-of-margins-has-changed"></a>WPF-Layout der Ränder Rundung wurde geändert.

|   |   |
|---|---|
|Details|Die Art und Weise, wie Ränder und die Grenzen und der Hintergrund darin geglättet werden, hat sich geändert. Auswirkungen durch diese Änderung:<ul><li>Die Breite oder Höhe der Elemente vergrößert oder verkleinert sich allenfalls um einen Pixel.</li><li>Die Platzierung eines Objekts kann sich allenfalls um einen Pixel verschieben.</li><li>Zentrierte Elemente können sich vertikal oder horizontal um allenfalls ein Pixel von der Mitte verschieben.</li></ul>Standardmäßig wird dieses neue Layout nur für Apps aktiviert, die auf .NET Framework 4.6 abzielen.|
|Vorschlag|Da diese Änderung Clipping die Rechte oder Unterseite von WPF-Steuerelementen bei hohen DPIs zu vermeiden tendenziell, apps, die auf frühere Versionen von .NET Framework aber auf .NET Framework 4.6 ausgeführt werden können auf Registrierungsbasis dieses neue Verhalten durch Hinzufügen der folgenden Zeile den <code>&lt;runtime&gt;</code> Abschnitt der Datei "App.config": <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>Apps, die .NET Framework 4.6 abzielen, aber WPF-Steuerelemente zum Rendern des vorherigen layoutalgorithmus verwenden soll dazu die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> Abschnitt der Datei "App.config": <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|Bereich|Gering|
|Version|4.6|
|Typ|Neuzuweisung|

