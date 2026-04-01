# Organização sugerida do repositório

Este guia propõe uma estrutura simples para manter o estudo de C++ separado da nova trilha de microcontroladores.

## Estrutura recomendada

```text
Cpp/
├── aulas/
│   ├── modulo01_introducao/
│   └── ...
├── exercicios/
│   ├── modulo01/
│   └── ...
├── projetos/
│   └── microcontroladores/
│       ├── pic/
│       ├── pic18/
│       ├── dspic/
│       ├── picavr/
│       ├── stm32/
│       └── esp32/
└── docs/
    └── ORGANIZACAO_REPOSITORIO.md
```

## Padrão para cada projeto de microcontrolador

Dentro de cada família (`pic`, `stm32`, `esp32`, etc.), use um projeto por pasta:

```text
projetos/microcontroladores/stm32/
└── blink_led/
    ├── README.md
    ├── src/
    ├── include/
    ├── docs/
    └── tools/
```

### Convenções úteis

- Nome de pasta em minúsculo e com `_` (ex.: `controle_motor_pwm`).
- `README.md` obrigatório em cada projeto com:
  - objetivo,
  - placa usada,
  - compilador/IDE,
  - pinagem,
  - como compilar e gravar.
- Sempre separar:
  - **código-fonte** (`src/`, `include/`),
  - **documentação** (`docs/`),
  - **scripts/ferramentas** (`tools/`).

## Sugestão para suas próximas trilhas

Com base no seu plano, você pode usar esta sequência:

1. `10.0 PIC` → `projetos/microcontroladores/pic`
2. `10.1 PIC18` → `projetos/microcontroladores/pic18`
3. `10.2 dsPIC` → `projetos/microcontroladores/dspic`
4. `10.3 PICAVR` → `projetos/microcontroladores/picavr`
5. `10.4 STM32` → `projetos/microcontroladores/stm32`
6. `10.5 ESP32` → `projetos/microcontroladores/esp32`

## Checklist rápido para manter organização

- [ ] Todo projeto tem `README.md` com instruções.
- [ ] Todo projeto compila com um comando documentado.
- [ ] Nomes de pastas seguem padrão único.
- [ ] Código e documentação estão separados.
- [ ] Projetos finalizados têm lições aprendidas em `docs/`.
