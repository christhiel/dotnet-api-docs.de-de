### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 ist eine 4.5.x.x-Version nicht verwenden, wenn selbst in der Registrierung registrieren

|   |   |
|---|---|
|Details|Wie zu erwarten wäre, wird der versionsschlüssel in der Registrierung festgelegt (am <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) für .NET Framework 4.6 "4.6" nicht "4,5" beginnt. Apps, die auf diesen Registrierungsschlüssel zu wissen, welche .NET Framework-Versionen auf einem Computer installiert werden sollte aktualisiert werden, um zu verstehen, dass 4.6 eine neue mögliche Version ist und eine, die kompatibel mit früheren 4.5.x loslässt.|
|Vorschlag|Update-apps, die Suche nach einem .NET Framework 4.5 installieren, indem Sie zu akzeptieren, sondern auch 4.6 4.5 Registrierungsschlüssel sucht.|
|Bereich|Edge|
|Version|4.6|
|Typ|Laufzeit|

