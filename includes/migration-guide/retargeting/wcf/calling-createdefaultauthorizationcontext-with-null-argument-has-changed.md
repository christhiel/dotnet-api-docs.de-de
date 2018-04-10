### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Aufrufen von CreateDefaultAuthorizationContext mit einem null-Argument wurde geändert.

|   |   |
|---|---|
|Details|Die Implementierung von der <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> zurückgegeben, die durch einen Aufruf der <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> mit einer null AuthorizationPolicies Argument entsprechende Implementierung in .NET Framework 4.6 geändert hat.|
|Vorschlag|In seltenen Fällen liegen bei WCF-Apps, die die benutzerdefinierte Authentifizierung verwenden, möglicherweise Verhaltensunterschiede vor. In derartigen Fällen gibt es zwei Möglichkeiten, um das vorherige Verhalten wiederherzustellen:<ol><li>Kompilieren Sie Ihre App erneut, damit sie auf eine frühere Version als .NET Framework 4.6 abzielt. Für IIS-gehostete Dienste verwenden die &lt;HttpRuntime TargetFramework =&quot;x.x&quot;  / &gt; Element an eine frühere Version von .NET Framework abzielen.</li><li>Fügen Sie dem Abschnitt <code>&lt;appSettings&gt;</code> Ihrer Datei „app.config“ die folgende Zeile hinzu: <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|Bereich|Gering|
|Version|4.6|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

