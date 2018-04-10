### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal.SizeOf und Marshal.PtrToStructure Überladungen unterbrechen dynamischen code

|   |   |
|---|---|
|Details|Ab .NET Framework 4.5.1, dynamisch binden an die Methoden <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, oder <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>, (über Windows PowerShell, IronPython oder die C#-dynamisches Schlüsselwort, z. B.) kann dazu führen, <code>MethodInvocationExceptions</code> daran, dass neue Überladungen dieser Methoden, die möglicherweise mehrdeutig für den Skriptmodulen hinzugefügt wurde.|
|Vorschlag|Aktualisieren Sie Skripts, um klar anzugeben, welche Überladung verwendet werden soll. Dies kann in der Regel dadurch erreicht werden, dass die Typparameter der Methoden explizit zu <xref:System.Type> umgewandelt werden. Weitere Informationen und Beispiele zur Problemumgehung finden Sie über [diesen Link](https://support.microsoft.com/kb/2909958/).|
|Bereich|Gering|
|Version|4.5.1|
|Typ|Laufzeit|

