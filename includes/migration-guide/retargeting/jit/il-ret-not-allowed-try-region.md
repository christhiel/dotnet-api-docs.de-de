### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret in einer Region, versuchen Sie es nicht zulässig.

|   |   |
|---|---|
|Details|Im Gegensatz zum JIT64-just-in-Time-Compiler lässt keine "ryujit" (in .NET 4.6 verwendet) zu einem IL ret Anweisung in einer Region, versuchen Sie es. Zurückgeben aus einem Try-Region durch die ECMA-335-Spezifikation nicht zulässig ist, und kein bekannter verwalteter Compiler generiert eine solche IL. Allerdings führt der JIT64-Compiler solche IL aus, wenn sie mithilfe von Reflektionsausgabe generiert wurde.|
|Vorschlag|Wenn eine app IL, die eine Ret-Opcode in einer Try-Region enthält generiert, kann die app als Ziel .NET 4.5 so verwenden die alte JIT und vermeiden diese Unterbrechung. Alternativ kann die generierte IL aktualisiert werden, um nach dem Try-Bereich zurückzugeben.|
|Bereich|Edge|
|Version|4.6|
|Typ|Neuzuweisung|

