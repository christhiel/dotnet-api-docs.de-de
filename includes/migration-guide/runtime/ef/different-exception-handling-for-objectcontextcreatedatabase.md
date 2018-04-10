### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>Verschiedene Ausnahmebehandlung für ObjectContext.CreateDatabase und DbProviderServices.CreateDatabase-Methode

|   |   |
|---|---|
|Details|Ab .NET 4.5 versuchen <code>CreateDatabase</code>-Methoden eine leere Datenbank zu löschen, wenn die Datenbankerstellung fehlgeschlagen ist. Wenn dieser Vorgang erfolgreich ist, wird die ursprüngliche <xref:System.Data.SqlClient.SqlException?displayProperty=name> verbreitet (anstelle der <xref:System.InvalidOperationException?displayProperty=name>, die in .NET 4.0 immer ausgelöst wurde).|
|Vorschlag|Beim Abfangen einer <xref:System.InvalidOperationException?displayProperty=name> während der Ausführung <xref:System.Data.Objects.ObjectContext.CreateDatabase> oder <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, sich sollte jetzt auch abgefangen werden.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

