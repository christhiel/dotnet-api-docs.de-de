### <a name="wpf-pointer-based-touch-stack"></a>WPF-Zeigerbasierten Touch-Stapel

|   |   |
|---|---|
|Details|Diese Änderung fügt die Fähigkeit, eine optionale WM_POINTER ermöglichen WPF Touch/Tablettstift Stapel basierend auf.  Entwickler, die nicht explizit dies aktivieren sollte keine Änderung des Verhaltens der WPF-Touch/Tablettstift angezeigt werden. Bekannte Probleme mit optionalen WM_POINTER aktuelle basierend Touch/Tablettstift Stapel:<ul><li>Keine Unterstützung für Freihand in Echtzeit.</li><li>Während der Freihandeingabe StylusPlugins weiterhin funktionieren, und sie verarbeitet werden im UI-Thread was zu Leistungseinbußen führen kann.</li><li>Verhaltensänderungen aufgrund von Änderungen bei der heraufstufung von Touch/Stiftereignisse Mausereignisse</li><li>Bearbeitung kann sich anders verhalten.</li><li>Drag & Drop wird für die Fingereingabe geeignetes Feedback nicht angezeigt werden.</li><li>Dies wirkt sich nicht Stifteingabe</li><li>Drag & Drop können auf Touch/Stylus-Ereignisse nicht mehr initiiert werden</li><li>Dadurch kann es möglicherweise zu einem Hängen der Anwendung kommen, bis die Mauseingabe erkannt wird.</li><li>Stattdessen sollten Entwickler Drag & Drop über Mausereignisse einleiten.</li></ul>|
|Vorschlag|Entwickler, die dieser Stapel aktivieren möchten können hinzufügen/Folgendes verwenden, um ihre "App.config" der Anwendungsdatei ' Merge ':<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>Entfernen Sie diese, oder Festlegen des Werts auf "false" wird dieser optionalen Stapel deaktivieren. Bitte beachten Sie, dass dieser Stapel nur auf Ersteller-Update für Windows 10 und höher verfügbar ist.|
|Bereich|Edge|
|Version|4.7|
|Typ|Neuzuweisung|

