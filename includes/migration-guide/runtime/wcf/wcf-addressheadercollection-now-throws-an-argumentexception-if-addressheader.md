### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF-AddressHeaderCollection löst jetzt ArgumentException, wenn ein ' AddressHeader '-Element null ist.

|   |   |
|---|---|
|Details|Ab .NET Framework 4.7.1, die <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> löst der Konstruktor ein <xref:System.ArgumentException> Wenn eines der Elemente ist <code>null</code>. In der .NET Framework 4.7 und früher wird keine Ausnahme ausgelöst.|
|Vorschlag|Treten Kompatibilitätsprobleme mit dieser Änderung auf das .NET Framework 4.7.1 oder eine höhere Version, Sie können teilnehmen es durch die folgende Zeile zum Hinzufügen der <code>&lt;runtime&gt;</code> Abschnitt der Datei "App.config"::<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Bereich|Gering|
|Version|4.7.1|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

