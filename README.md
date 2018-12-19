# E5R Hackathon

Desafios para Hackathon E5R.

Para cada desafio, você deve tornar a síntaxe na classe `Hackathon` implementando a
classe `HackathonChallenge`.

A regra básica é: *A classe `Hackathon` não deve ser alterada*

Além da regra básica, cada desafio impõe suas próprias regras que também devem ser
obedecidas.

```csharp
class HackathonChallenge
{
    /* TODO... */
}
```

## Desafio 1 - Callback

Regras:
* Só faça funcionar!

```csharp
class Hackathon : HackathonChallenge
{
    public Hackathon()
    {
        Feature("Somar")
               ("Calcula a soma entre números inteiros,")
               ("produzindo resultados matematicamente coerentes.")
        ;
    }
}


```

## Desafio 2 - Operações matemáticas básicas

Regras:
* Os únicos operadores matemáticos permitidos são `+` e `-`.

```csharp
class Hackathon : HackathonChallenge
{
    public Hackathon()
    {
        // 2 + 2 = 4
        Assert(
            Soma(2, 2) == 4
        );

        // 4 - 2 = 2
        Assert(
            Subtrai(4, 2) == 2
        );

        // 5 * 2 = 10
        Assert(
            Multiplica(5, 2) == 10
        );

        // 12 / 3 = 4
        Assert(
            Divide(12, 3) == 4
        );

        bool errouDivisao = false;

        // 10 / 0 = !{erro de divisão por zero}
        try { Divide(10, 0); }
        catch (DivideByZeroException) { errouDivisao = true; }

        Assert(errouDivisao);
    }
}
```
