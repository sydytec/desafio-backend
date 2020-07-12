# Desafio Técnico Vaga Backend

Por conta do coronavírus, os principais campeonatos de futebol estão paralisados. Minha agência de apostas tem sofrido com a queda de faturamento. Pensando nisso, elaboramos um fantasy game, onde os apostadores escolhem times, e esses times se enfrentam em uma partida em que o resultado é imprevisível. Pensando nisso, você precisa criar uma API onde é possível gerenciar os times cadastrados (Cadastrar, Editar, Remover, Visualizar) e realizar campeonatos. Nesses campeonatos todos os times cadastrados se enfrentam, você deve gerar um placar randomizado para cada partida. Para cada campeonato, você deve informar o campeão, o vice-campeão e o terceiro colocado. O campeão será aquele com o maior número de pontos.

Os nomes dos times devem ter ao menos 3 caracteres, e não devem existir times com nomes iguais.

Pontuação das partidas:

- Derrota = 0
- Empate = 1
- Ganhador = 3

Exemplos de endpoints que entregariam os requisitos :

## Times

```json
POST /api/Time

body:
{
    "nome": "Sydy"
}
```

```json
PUT /api/Time/{id}

body:
{
    "nome": "Sydy Editado"
}
```

```
DELETE /api/Time/{id}
```

GET /api/Time/{id}

Resposta:

```json
{
    "id": "1",
    "nome": "Sydy Editado"
}
```

GET /api/Time

params:
pagina:1
tamanhoPagina: 10

Resposta:

```json
{
    "pagina": 1,
    "tamanhoPagina": 10,
    "qtdPagina": 3,
    "itens": [
        {
            "id": "1",
            "nome": "Sydy Editado"
        }
    ]
}
```

## Campeonato

GET /api/Campeonato

```json
{
    "partidas": [
        {
            "times": "Time 01 x Time 02",
            "resultado": "1 x 0"
        },
        {
            "times": "Time 01 x Time 03",
            "resultado": "1 x 1"
        },
        {
            "times": "Time 01 x Time 04",
            "resultado": "3 x 1"
        },
        {
            "times": "Time 02 x Time 03",
            "resultado": "1 x 5"
        },
        {
            "times": "Time 02 x Time 04",
            "resultado": "3 x 1"
        },
        {
            "times": "Time 03 x Time 04",
            "resultado": "1 x 4"
        }
    ],
    "campeao": "Time 01",
    "vice": "Time 03",
    "terceiro": "Time 02"
}
```

Requisitos:

- Use ASP.NET Core 3.1 WebAPI
- Use EntityFramework Core
- Use CodeFirst
- Use o banco de dados SQL Server (pode ser local)

O que nós avaliaremos:

- Boa utilização de Orientação à Objetos
- Boa estrutura de pasta e arquivos
- Capacidade de escrever código coeso e legível

Você é livre para utilizar a biblioteca que desejar, adicionar/alterar funcionalidades, e etc.

> "A criatividade são as asas do homem"
> (Oliveira, Oliveira, Gonçalves, Silva, Silva, Monet e Procopiou; 2020)

Você tem 7 dias para a conclusão do teste. Se concluir antes sinta-se a vontade para enviar antes desse prazo.

Você deve enviar o link do seu repositório público para o [mecontrata@sydy.com.br](mailto:mecontrata@sydy.com.br?subject=Desafio%20Técnico%20Backend&body=Segue%20o%20meu%20desafio%20técnico,%20a%20implementação%20se%20encontra%20em:%20).