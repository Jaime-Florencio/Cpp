# Convenções de Organização

## Pastas
- Use minúsculas e hífen: `nome-da-pasta`.
- Preserve ordem didática com prefixo numérico: `01-`, `02-`, ...

## Arquivos `.cpp`
- Aula/exemplo: `01-nome-do-exemplo.cpp`
- Exercício: `ex-01-nome-curto.cpp`
- Projeto: `main.cpp`, `app.cpp`, `modulo-io.cpp`, `http-client.cpp`

## Organização por aula
Cada aula deve conter:
- `README.md`
- `exemplos/`
- `exercicios/`

## Exercícios
Dentro de `exercicios/`, prefira:
- `ex-01-enunciado.md`
- `ex-01-resolucao.cpp`

## Projetos
Dentro de `projects/`:
- `general/` para projetos amplos de estudo
- `embedded/` para AVR/ESP32/MSP430/STM32 e similares

Estrutura sugerida por projeto:
- `README.md`
- `src/`
- `include/` (opcional)
- `docs/` (opcional)
