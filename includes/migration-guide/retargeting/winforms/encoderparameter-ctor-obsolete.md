### <a name="encoderparameter-ctor-is-obsolete"></a>EncoderParameter Ctor ist veraltet

|   |   |
|---|---|
|Details|Der <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>-Konstruktor ist jetzt veraltet und gibt Buildwarnungen aus, wenn er verwendet wird.|
|Vorschlag|Obwohl die <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>Konstruktor sind weiterhin funktionsfähig, der folgende Konstruktor sollte stattdessen verwendet werden, um die veraltete Buildwarnung zu vermeiden, beim erneuten Kompilieren von Code mit .NET 4.5-Tools: <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.|
|Bereich|Gering|
|Version|4.5|
|Typ|Neuzuweisung|
|Betroffene APIs|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

