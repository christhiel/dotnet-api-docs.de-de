### <a name="chained-popups-with-staysopenfalse"></a>Verkettet Popups mit "StaysOpen" = "false"

|   |   |
|---|---|
|Details|Ein Popup mit "StaysOpen" = "false" sollte auf Schließen, wenn Sie außerhalb des Popups klicken. Wenn zwei oder mehr solcher Popups verkettet sind (d. h. eine enthält eine andere), es wurden viele Probleme, einschließlich:<ul><li>Öffnen Sie zwei Ebenen zu, klicken Sie auf außerhalb P2, aber in P1.  Nichts geschieht.</li><li>Öffnen Sie zwei Ebenen zu, klicken Sie auf externe P1.  Schließen Sie beide Popups.</li><li>Öffnen Sie und schließen Sie zwei Ebenen.  Wiederholen Sie dann, P2 erneut zu öffnen.  Nichts geschieht.</li><li>Versuchen Sie drei Ebenen zu öffnen.  Ist nicht möglich.  (Geschieht nichts oder die ersten beiden Stufen schließen, je nachdem, wo Sie klicken.) Diese Fälle (und andere Variationen) jetzt wie erwartet funktionieren.</li></ul>|
|Bereich|Edge|
|Version|4.7.1|
|Typ|Laufzeit|
|Betroffene APIs|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

