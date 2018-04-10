### <a name="winforms-checkforoverflowunderflow-property-is-now-true-for-systemdrawing"></a>WinForm CheckForOverflowUnderflow-Eigenschaft gilt für "System.Drawing"

|   |   |
|---|---|
|Details|Die CheckForOverflowUnderflow-Eigenschaft für die Assembly System.Drawing.dll festgelegt ist auf "true".|
|Vorschlag|Zuvor wurde das Ergebnis im Fall von Überläufen automatisch abgeschnitten. Nun wird eine <xref:System.OverflowException?displayProperty=name>-Ausnahme ausgelöst.|
|Bereich|Edge|
|Version|4.5|
|Typ|Laufzeit|

