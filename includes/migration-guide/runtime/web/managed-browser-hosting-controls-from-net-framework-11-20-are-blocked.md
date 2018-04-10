### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>Hosten von Steuerelementen aus .NET Framework 1.1 und 2.0 verwaltete Browser werden blockiert.

|   |   |
|---|---|
|Details|Das Hosting dieser Steuerelemente wird in Internet Explorer blockiert.|
|Vorschlag|Internet Explorer kann eine Anwendung, die verwaltete Browserhostingsteuerelemente verwendet, nicht starten. Das vorherige Verhalten kann wiederhergestellt werden, indem der EnableIEHosting-Wert des Registrierungsunterschlüssels festlegen <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> zu <code>1</code> für X86 Systeme und für 32-Bit-Prozesse auf X64-Systemen und durch Festlegen der <code>EnableIEHosting</code> Wert des Registrierungsunterschlüssels <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>zu <code>1</code> für 64-Bit-Prozesse auf X64 Systeme.|
|Bereich|Gering|
|Version|4.5|
|Typ|Laufzeit|

