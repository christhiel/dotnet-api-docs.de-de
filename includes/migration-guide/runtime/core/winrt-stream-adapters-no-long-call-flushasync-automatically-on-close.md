### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a>WinRT-streamadapter Aufrufen nicht mehr FlushAsync automatisch schließen

|   |   |
|---|---|
|Details|In Windows Store-apps aufrufen Windows-Runtime-streamadapter nicht mehr von der Dispose-Methode der FlushAsync-Methode auf.|
|Vorschlag|Diese Änderung sollte transparent sein. Entwickler können das vorherige Verhalten wiederherstellen, indem sie Code wie den folgenden schreiben:<pre><code class="language-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|Bereich|Transparent|
|Version|4.5.1|
|Typ|Laufzeit|

