# 📘 Aula 1.3 – Primeiro Contato com Classes em C++

## 🎯 Objetivo
Compreender o conceito de **classes e objetos** em C++, entender a lógica da **Programação Orientada a Objetos (POO)** e analisar cada linha do código desenvolvido.

---

## 🔹 1. O que é uma Classe?
Uma **classe** é um **molde (modelo)** que define o que um tipo de objeto pode fazer e quais informações ele guarda.  
Ela combina **dados** (variáveis internas, chamadas *atributos*) e **funções** (chamadas *métodos*) que atuam sobre esses dados.

💡 **Analogia:**  
Imagine uma **receita de bolo**.  
A receita define **os ingredientes e o modo de preparo** (a estrutura), mas **não é o bolo em si**.  
Quando você segue a receita, cria um **bolo real** — isto é, um **objeto**.

---

## 🔹 2. O que é um Objeto?
Um **objeto** é uma **instância concreta** de uma classe.  
Quando você cria um objeto, o programa reserva espaço na memória para ele e permite acessar os métodos e atributos definidos pela classe.

Exemplo:
```cpp
class Carro {
public:
    string cor;
    int ano;
    void buzinar() {
        cout << "Biiiii!" << endl;
    }
};

int main() {
    Carro meuCarro;
    meuCarro.cor = "vermelho";
    meuCarro.ano = 2020;
    meuCarro.buzinar();
}
```
➡️ Aqui:  
- `Carro` é a **classe**.  
- `meuCarro` é o **objeto**.  
- `cor` e `ano` são **atributos**.  
- `buzinar()` é um **método** (função dentro da classe).  

---

## 🔹 3. Diferença entre C e C++
Em **C**, a programação é **procedural**: o foco é em funções isoladas que operam sobre dados.  
Em **C++**, é **orientada a objetos**: o foco é em entidades (classes) que contêm dados e comportamentos.

| C (Procedural) | C++ (Orientado a Objetos) |
|----------------|----------------------------|
| Baseado em funções | Baseado em classes e objetos |
| Dados e funções separados | Dados e funções agrupados |
| Foco em "como fazer" | Foco em "quem faz o quê" |

---

## 🔹 4. Análise do Código da Aula 1.3

### 🧩 Cabeçalho e Inclusões
```cpp
#include <iostream>
using std::cout;
using std::cin;
using std::endl;
```
- `#include <iostream>`: importa as funções de entrada e saída (`cin`, `cout`, `endl`).
- `using std::cout;` → evita ter que escrever `std::cout` sempre.  
  Exemplo: `cout << "Olá";` em vez de `std::cout << "Olá";`.

---

### 🧩 Trabalhando com Strings
```cpp
#include <string>
using std::string;
using std::getline;
```
- `#include <string>`: permite usar variáveis do tipo texto.  
- `getline(cin, variavel)`: lê uma linha inteira, **incluindo espaços**.

Sem `getline`, o comando `cin` pararia na primeira palavra.

---

### 🧩 Desenvolvimento da Classe
```cpp
class SalesScore {
public:
    void bootSystem(string storeTitle) {
        cout << "Score de Vendas!\n" << storeTitle << endl;
    }
};
```
**Linha a linha:**  
- `class SalesScore`: cria uma nova classe chamada *SalesScore*.
- `public:`: define que o método abaixo pode ser acessado fora da classe.
- `void bootSystem(string storeTitle)`: cria o método (função) da classe.  
  - `void`: não retorna valor.  
  - `storeTitle`: parâmetro que recebe o nome da loja digitado pelo usuário.
- Dentro da função, `cout` mostra mensagens na tela.

💡 Uma **função dentro da classe** é chamada de **método**.

---

### 🧩 Função Principal (main)
```cpp
int main() {
    string storeTitle;
    SalesScore mySales;

    cout << "Insira o nome da Loja:" << endl;
    getline(cin, storeTitle);
    cout << endl;

    mySales.bootSystem(storeTitle);

    while (1);
    return 0;
}
```

**Explicando cada trecho:**  
1. `string storeTitle;` → cria uma variável de texto para guardar o nome da loja.  
2. `SalesScore mySales;` → cria um objeto chamado `mySales` a partir da classe `SalesScore`.  
3. `getline(cin, storeTitle);` → lê o nome completo da loja (com espaços).  
4. `mySales.bootSystem(storeTitle);` → chama o método da classe, exibindo o título no console.  
5. `while(1);` → mantém o programa aberto (apenas para fins de teste).  
6. `return 0;` → indica que o programa terminou corretamente.

---

## 🔹 5. Saída Esperada

```
Insira o nome da Loja:
Loja Central Ponta Grossa

Score de Vendas!
Loja Central Ponta Grossa
```

---

## 🔹 6. A Lógica por Trás das Classes

Quando o programa executa:
1. A classe `SalesScore` é um molde com uma função (`bootSystem`).  
2. O objeto `mySales` é criado a partir dessa classe.  
3. O usuário digita o nome da loja.  
4. O método `bootSystem()` é chamado e imprime o título.  

💡 A vantagem é que, no futuro, a classe pode ganhar mais funções (como calcular vendas, gerar relatórios etc.), e o código principal (`main`) **não precisa mudar**.

---

## 🔹 7. Por Que Usar Classes?
| Vantagem | Explicação |
|-----------|------------|
| Organização | Agrupa funções e dados relacionados. |
| Reutilização | Pode criar vários objetos da mesma classe. |
| Expansão | Pode adicionar métodos sem mudar o código principal. |
| Clareza | Cada classe representa um conceito do mundo real. |

---

## 🧭 Resumo Final

| Conceito | Definição |
|-----------|-----------|
| **Classe** | Molde que define atributos e comportamentos. |
| **Objeto** | Instância concreta da classe. |
| **Método** | Função definida dentro de uma classe. |
| **Atributo** | Dado armazenado dentro da classe. |
| **public / private** | Controla quem pode acessar os métodos e variáveis. |
| **POO (Programação Orientada a Objetos)** | Paradigma que agrupa dados e funções em classes e objetos. |

---

📘 **Conclusão:**  
A classe é uma forma de **organizar e estruturar o pensamento do programador**.  
Ela permite representar o mundo real dentro do código: lojas, pessoas, contas, carros, produtos, sensores etc.  
Cada classe é um “modelo”, e cada objeto é uma “instância viva” desse modelo, que interage com o restante do programa.
