### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>SQL-Workflowpersistenz fügt Primärschlüssel-Clustern und lässt keine null-Werte in bestimmte Spalten

|   |   |
|---|---|
|Details|Beginnend mit der .NET Framework-4.7, verwenden Sie die Tabellen, die für SQL Workflow Instanz Store (SWIS) vom Skript SqlWorkflowInstanceStoreSchema.sql erstellten gruppierten Primärschlüssel. Aus diesem Grund Identitäten unterstützen keine <code>null</code> Werte. Der Vorgang des SWIS wird durch diese Änderung nicht beeinträchtigt. Die Updates wurden zur Unterstützung von SQL Server-Transaktionsreplikation.|
|Vorschlag|Die SQL-Datei SqlWorkflowInstanceStoreSchemaUpgrade.sql muss zu vorhandenen Installationen angewendet werden, damit diese Änderung auftreten. Neue Datenbank-Installationen müssen die Änderung automatisch.|
|Bereich|Edge|
|Version|4.7|
|Typ|Laufzeit|

