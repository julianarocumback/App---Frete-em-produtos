## Preço para encomendas

**Enunciado:** Imagine que você e sua equipe foram contratados por uma empresa de logística que acabou de entrar no ramo. Essa empresa trabalha com encomendas de pequeno e médio porte e opera somente entre 3 cidades.

O valor que a empresa cobra por objeto é dado pela seguinte equação: **(dimensão * peso * rota)**

Em que cada uma das variáveis que compõe o preço total é quantizada da seguinte maneira:

**Quadro 1**
|      Dimensões (cm³)      |   Valor (R$)   |
|:-------------------------:|:--------------:|
|       volume < 1000       |      10,00     |
|   1000 <= volume < 10000  |      20,00     |
|  10000 <= volume < 30000  |      30,00     |
|  30000 <= volume < 100000 |      50,00     |
|     volume >= 100000      |  Não é aceito  |

**Quadro 2**
|     Peso (kg)     |  Multiplicador | 
|:-----------------:|:--------------:|
|    peso <= 0.1    |        1       |
|  0.1 <= peso < 1  |       1.5      |
|   1 <= peso < 10  |        2       |
|  10 <= peso < 30  |        3       |
|     peso => 30    |  Não é aceito  |

**Quadro 3**
|                  Rota                  |  Multiplicador  | 
|:--------------------------------------:|:---------------:|
|  RS - Rio de Janeiro até São Paulo     |        1        |
|  SR - São Paulo até Rio de Janeiro     |        1        |
|  BS - Brasília até São Paulo           |       1.2       |
|  SB - São Paulo até Brasília           |       1.2       |
|  BR - Brasília até Rio de Janeiro      |       1.5       |
|  RB - Rio de Janeiro até Brasília      |       1.5       |

Obs.: Pode-se mudar o nome das cidades e siglas.

**Elabore um programa em Python que:**

* Pergunte a **altura (cm)**, **comprimento (cm)** e **largura (cm)** do objeto. Se for digitado um valor não numérico e/ou as dimensões passarem do limite aceito, repita a pergunta;
* Pergunte o **peso do objeto (kg)**. Se for digitado um valor não numérico e/ou o peso passar do limite aceito, repita a pergunta;
* Pergunte a **rota do objeto**. Se for digitado uma opção que não esteja na tabela, repita a pergunta;
* Encerre o total a ser pago com base na equação desse enunciado; 
* Deve-se codificar uma função '**dimensoesObjeto**' **(exigência 1 de 3)**;
    * Dentro da função, pergunte a **altura** do objeto (cm); 
    * Dentro da função, pergunte o **comprimento** do objeto (cm); 
    * Dentro da função, pergunte a **largura** do objeto (cm);
    * Calcule o **volume (cm)** da caixa p/a objeto (altura * largura * comprimento); 
    * Deve-se ter **try/except** para o caso do usuário digitar um valor não numérico; 
    * Deve-se retornar o **valor em (R$)** conforme o Quadro 1.
* Deve-se codificar uma função '**pesoObjeto**' **(exigência 2 de 3)**;
    * Dentro da função, pergunte o **peso** do objeto (kg); 
    * Deve-se ter um **try/except** para o caso do usuário digitar um valor não numérico; 
    * Deve-se retornar o **multiplicador** conforme o Quadro 2.
* Deve-se codificar uma função '**rotaObjeto**' **(exigência 3 de 3)**.
    * Dentro da função, pergunte a **rota** desejada (sugestão: utilize as siglas para facilitar os testes); 
    * Deve-se retornar o **multiplicador** conforme o Quadro 3.

**Teste:**

* Colocar um exemplo de SAIDA DE CONSOLE uma encomenda com peso, dimensões e rota válidos.
* Colocar um exemplo de SAIDA DE CONSOLE com o tratamento de erro quando digitado um valor não numérico é digitado no campo peso ou dimensões.

---

**Saída do console:**

![alt text](img/terminal.png)