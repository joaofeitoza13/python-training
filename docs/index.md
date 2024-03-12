# Notas Musicais

![ logo_do_projeto ]( assets/logo.png ){ width="300" .center }

## Como usar?

Notas musicais é um CLI para ajudar na formação de escalas e acordes.

Toda a aplicação é baseada em um comando chamado ```notas-musicais```. Esse comando tem subcomandos relacionados a cada ação que a aplicação pode realizar: ```escalas``` e ```acordes```.

```bash
poetry run notas-musicais escala
```

Retornando os graus e as notas correspondentes a essa escala:

```bash
┏━━━┳━━━━┳━━━━━┳━━━━┳━━━┳━━━━┳━━━━━┓
┃ I ┃ II ┃ III ┃ IV ┃ V ┃ VI ┃ VII ┃
┡━━━╇━━━━╇━━━━━╇━━━━╇━━━╇━━━━╇━━━━━┩
│ C │ D  │ E   │ F  │ G │ A  │ B   │
└───┴────┴─────┴────┴───┴────┴─────┘

```

### Alteração na escala

O primeiro parâmetro do CLI é a tônica da escala que deseja exibir. Desta forma, você pode alterar a escala retornada. Por exemplo, a escala de F#:

```bash
poetry run notas-musicais escala F# maior
```

Resultado em:

```bash
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ F# │ G# │ A#  │ B  │ C# │ D# │ F   │
└────┴────┴─────┴────┴────┴────┴─────┘
```

### Alteração na tonalidade da escala

Você pode alterar a tonalidade da escala também! Esse é o segundo parâmetro da linha de comando. Por exemplo, a escala de D# maior:

```bash
poetry run notas-musicais escala D# menor
```

```bash
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ D# │ F  │ F#  │ G# │ A# │ B  │ C#  │
└────┴────┴─────┴────┴────┴────┴─────┘
```

## Acordes

Uso básico

```bash
{{ commands.run }} acorde
┏━━━┳━━━━━┳━━━┓
┃ I ┃ III ┃ V ┃
┡━━━╇━━━━━╇━━━┩
│ C │ E   │ G │
└───┴─────┴───┘
```

### Variações na cifra

```bash
{{ commands.run }} acorde C+
┏━━━┳━━━━━┳━━━━┓
┃ I ┃ III ┃ V+ ┃
┡━━━╇━━━━━╇━━━━┩
│ C │ E   │ G# │
└───┴─────┴────┘
```

Até o momento você usar acordes maiores, menores, dimunito e aumentados


## Mais informações sobre o CLI

Para descobrir outras opções, você pode usar a flag `--help`:

```bash
poetry run notas-musicais --help

Usage: escalas [OPTIONS] [TONICA] [TONALIDADE]                                      
                                                                                     
╭─ Arguments ──────────────────────────────────────────────────────────────────╮
│   tonica       [TONICA]      Tônica da escala       [default: c]             │
│   tonalidade   [TONALIDADE]  Tonalidade da escala   [default: maior]         │
╰──────────────────────────────────────────────────────────────────────────────╯
```
