### <a name="wpf-spell-checking-in-text-enabled-controls-will-not-work-in-windows-10-for-languages-not-in-the-oss-input-language-list"></a>WPF-Rechtschreibprüfungs in Text aktivierte Steuerelemente funktioniert in Windows 10 nicht für Sprachen, die nicht in der Betriebssystemliste Eingabesprache

|   |   |
|---|---|
|Details|Bei Ausführung auf Windows 10 funktionieren die Rechtschreibprüfung nicht für Text aktiviert WPF-Steuerelemente, da Plattform-rechtschreibungsfunktionen nur für Sprachen, die in der eingabesprachenliste vorhanden verfügbar sind. In Windows 10 Wenn die Liste der verfügbaren Tastaturen eine anderen Sprache hinzugefügt wird Windows automatisch heruntergeladen und installiert eine entsprechende Funktion Paket bei Bedarf (Feature-On), die Rechtschreibprüfung Funktionen bereitstellt. Durch das Hinzufügen der Sprache zur Eingabesprachenliste wird die Rechtschreibprüfung unterstützt.|
|Vorschlag|Denken Sie daran, dass die Sprache oder das Text-der Rechtschreibprüfung werden als eine Eingabesprache für die Rechtschreibprüfung, Informationen zum Arbeiten in Windows 10 hinzugefügt werden muss.|
|Bereich|Edge|
|Version|4.6|
|Typ|Laufzeit|

