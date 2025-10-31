# 🧮 Exercício 1.2 – Entrada de Dados e Operações Aritméticas em C++

## 🎯 Objetivo
Criar um programa em **C++** que:
1. Solicite **dois números** ao usuário.  
2. Calcule e exiba:
   - A **soma** dos números.  
   - A **diferença** entre eles.  
   - A **divisão** entre eles.  
3. Informe se o **primeiro número** é maior, menor ou igual ao segundo.

---

## 🧠 Conceitos utilizados
- **Entrada de dados:** `std::cin`
- **Saída de dados:** `std::cout`
- **Quebra de linha:** `std::endl` ou `\n`
- **Estrutura condicional:** `if`, `else if`, `else`
- **Operações aritméticas:** `+`, `-`, `/`

---

## 💻 Código do Programa

```cpp
#include <iostream>

int main()
{
    float valor1, valor2, soma, diferenca, divisao;

    std::cout << "Digite o valor 1: " << std::endl;
    std::cin >> valor1;

    std::cout << "Digite o valor 2: " << std::endl;
    std::cin >> valor2;

    soma = valor1 + valor2;
    diferenca = valor1 - valor2;
    divisao = valor1 / valor2;

    std::cout << "\nResultados:\n";
    std::cout << "Soma: " << soma << std::endl;
    std::cout << "Diferenca: " << diferenca << std::endl;
    std::cout << "Divisao: " << divisao << std::endl;

    if (valor1 > valor2)
        std::cout << valor1 << " é maior que " << valor2 << std::endl;
    else if (valor1 < valor2)
        std::cout << valor1 << " é menor que " << valor2 << std::endl;
    else
        std::cout << "Os dois valores são iguais." << std::endl;

    while (1);
    return 0;
}
```

---

## 🧩 Explicação passo a passo

1. **Declaração das variáveis**
   ```cpp
   float valor1, valor2, soma, diferenca, divisao;
   ```
   - `float`: usado para permitir números com casas decimais.

2. **Leitura dos valores**
   ```cpp
   std::cin >> valor1;
   std::cin >> valor2;
   ```
   - `std::cin` lê o valor digitado e armazena na variável.

3. **Cálculos**
   ```cpp
   soma = valor1 + valor2;
   diferenca = valor1 - valor2;
   divisao = valor1 / valor2;
   ```
   - Cada operação aritmética é feita e salva em uma variável.

4. **Exibição dos resultados**
   ```cpp
   std::cout << "Soma: " << soma << std::endl;
   ```
   - `std::cout` mostra o resultado no console.

5. **Comparação**
   ```cpp
   if (valor1 > valor2)
       std::cout << valor1 << " é maior que " << valor2;
   else if (valor1 < valor2)
       std::cout << valor1 << " é menor que " << valor2;
   else
       std::cout << "Os dois valores são iguais.";
   ```

---

## 📘 Saída esperada (exemplo)

Entrada:
```
Digite o valor 1:
8
Digite o valor 2:
4
```

Saída:
```
Resultados:
Soma: 12
Diferenca: 4
Divisao: 2
8 é maior que 4
```

---

## 🧭 Observações
- Se quiser exibir mais casas decimais, inclua:
  ```cpp
  std::cout.precision(2);
  std::cout << std::fixed;
  ```
- Sempre use **UTF-8** para que acentos apareçam corretamente.
