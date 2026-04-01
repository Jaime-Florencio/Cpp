# Repositório de Estudos de C++

Estrutura pensada para estudo, revisão e evolução prática no GitHub.

## Visão geral

- `curso-cpp/topicos/`: trilha principal do curso (14 tópicos, 5 aulas por tópico)
- `curso-cpp/projects/`: projetos práticos finais (separados das aulas)
- `curso-cpp/templates/`: modelos reutilizáveis para novas aulas e projetos

## Índice do curso

1. [01-introducao](./curso-cpp/topicos/01-introducao)
2. [02-variaveis-e-tipos](./curso-cpp/topicos/02-variaveis-e-tipos)
3. [03-operadores](./curso-cpp/topicos/03-operadores)
4. [04-controle-de-fluxo](./curso-cpp/topicos/04-controle-de-fluxo)
5. [05-funcoes](./curso-cpp/topicos/05-funcoes)
6. [06-arrays-e-strings](./curso-cpp/topicos/06-arrays-e-strings)
7. [07-ponteiros-e-referencias](./curso-cpp/topicos/07-ponteiros-e-referencias)
8. [08-structs-e-enums](./curso-cpp/topicos/08-structs-e-enums)
9. [09-orientacao-a-objetos](./curso-cpp/topicos/09-orientacao-a-objetos)
10. [10-heranca-e-polimorfismo](./curso-cpp/topicos/10-heranca-e-polimorfismo)
11. [11-excecoes-e-debug](./curso-cpp/topicos/11-excecoes-e-debug)
12. [12-stl](./curso-cpp/topicos/12-stl)
13. [13-arquivos-e-modularizacao](./curso-cpp/topicos/13-arquivos-e-modularizacao)
14. [14-projeto-e-boas-praticas](./curso-cpp/topicos/14-projeto-e-boas-praticas)

## Estrutura padrão por aula

Cada aula segue este formato:

- `README.md` → teoria e resumo
- `exemplos/` → códigos de referência
- `exercicios/` → desafios da aula (quando houver)

> Decisão prática: manter `exercicios/` em todas as aulas deixa a navegação previsível.

## Convenção de nomes para arquivos `.cpp`

- Exemplos: `01-entrada-saida.cpp`, `02-if-else.cpp`
- Exercícios: `ex-01.cpp`, `ex-02.cpp`
- Projetos: `main.cpp`, `modulo-conversao.cpp`, `menu.cpp`

## Padrão para exercícios e projetos

- Exercício:
  - `enunciado.md`
  - `ex-01.cpp`
- Projeto:
  - `README.md`
  - `src/`
  - `docs/`
  - `include/` (opcional)

## CMake no futuro (sem complicar agora)

Quando quiser escalar, use um `CMakeLists.txt` por projeto em `curso-cpp/projects/`.
Um template inicial já foi adicionado em:

- [`curso-cpp/templates/projeto/CMakeLists.txt`](./curso-cpp/templates/projeto/CMakeLists.txt)
