### <a name="the-replace-method-in-odata-urls-is-disabled-by-default"></a>Die Replace-Methode in OData-URLs ist standardmäßig deaktiviert.

|   |   |
|---|---|
|Details|Ab .NET Framework 4.5 ist die Replace-Methode in OData-URLs standardmäßig deaktiviert. Wenn „Replace“ für OData (jetzt standardmäßig) deaktiviert ist, schlagen alle Benutzeranforderungen fehl, einschließlich der Ersetzungsfunktionen (die nicht üblich sind).|
|Vorschlag|Wenn die Replace-Methode erforderlich ist (Dies ist ungewöhnlich), es kann über eine Config-Einstellungen wieder aktiviert werden, (<xref:System.Data.Services.Configuration.DataServicesFeaturesSection.ReplaceFunction?displayProperty=name>). Eine aktivierte Replace-Methode kann jedoch Sicherheitslücken öffnen und sollte nur nach sorgfältiger Prüfung verwendet werden.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.Services.DataService%601?displayProperty=nameWithType></li></ul>|

