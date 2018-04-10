### <a name="machinekeyencode-and-machinekeydecode-methods-are-now-obsolete"></a>MachineKey.Encode und MachineKey.Decode Methoden sind jetzt veraltet

|   |   |
|---|---|
|Details|Diese Methoden sind jetzt veraltet. Die Kompilierung von Code, der diese Methoden aufruft, erzeugt eine Compilerwarnung.|
|Vorschlag|Die empfohlenen Alternativen sind <xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> und <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])>. Alternativ können die Erstellung angezeigten Warnungen unterdrückt werden, oder sie mit einem älteren Compiler vermieden werden können. Die APIs werden weiterhin unterstützt.|
|Bereich|Gering|
|Version|4.5|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Web.Security.MachineKey.Encode(System.Byte[],System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li><li><xref:System.Web.Security.MachineKey.Decode(System.String,System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li></ul>|

