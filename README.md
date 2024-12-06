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

## Desafio 3 - Paginação

Imagine uma lista de itens qualquer:
```cs
IList<object>;
```

Uma função que receba uma lista, um número de página atual, um número de registros por página,
um limite máximo para exibição de páginas, deve:

* Calcular o número de páginas possíveis dentro da lista fornecida;
* Retornar uma lista de páginas onde a página atual esteja o maix próximo possível do centro da lista;
* Não exceder o limite máximo de páginas a exibir;

Expectativa
```
maximoPaginaExibicao = 5
totalPaginas         = 10
paginaAtual          = 5

        1  2  3  4  5
      +---------------+
1, 2, | 3, 4, 5, 6, 7 |, 8, 9, 10
              |
              *

maximoPaginaExibicao = 5
totalPaginas         = 10
paginaAtual          = 2

  1  2  3  4  5
+---------------+
| 1, 2, 3, 4, 5 |, 6, 7, 8, 9, 10
     |
     *

maximoPaginaExibicao = 5
totalPaginas         = 10
paginaAtual          = 10

                  1  2  3  4  5
                +----------------+
1, 2, 3, 4, 5 , | 6, 7, 8, 9, 10 |
                              |
                              *
```

### Desafio 4 - Cron Jobs

Construa um executor de jobs tipo CRON

- Pense em um agendador de próximos passos
- Pense em um executor independente
- Pense em um sistema de log independente
- Pense em executar em containers

### Desafio 5 - Notas de lançamento Git

Construa um executável que seja capaz de ler um repositório git
de um commit em diante e montar um Markdown de notas de lançamento.

- Pense em [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)
- Pense em agrupamento de commits por tipo de contribuição
- Pense em links
- Pense em mais detalhes
- Pense em alertas de _breaking changes_
