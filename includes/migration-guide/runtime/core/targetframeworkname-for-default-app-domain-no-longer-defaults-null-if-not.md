### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>TargetFrameworkName für Standard-app-Domäne ist standardmäßig nicht mehr null, sofern nichts anderes festgelegt

|   |   |
|---|---|
|Details|Die <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> wurde zuvor in der Standardanwendungsdomäne null, sofern sie nicht explizit festgelegt wurde. 4.6, ab der <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> -Eigenschaft für die Standarddomäne für die app hat einen Standardwert von TargetFrameworkAttribute abgeleitet wird, (sofern vorhanden). Nicht standardmäßige app-Domänen erben weiterhin ihre <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> von der Standardanwendungsdomäne (die nicht auf null in 4.6 Standard wird), wenn sie explizit außer Kraft gesetzt wird.|
|Vorschlag|Der Code sollte aktualisiert werden, um nicht davon abhängig zu sein, dass <xref:System.AppDomainSetup.TargetFrameworkName> standardmäßig NULL verwendet. Wenn es erforderlich ist, dass diese Eigenschaft weiterhin zu NULL ausgewertet wird, kann dieser Wert explizit festgelegt werden.|
|Bereich|Edge|
|Version|4.6|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

