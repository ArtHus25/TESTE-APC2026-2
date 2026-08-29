# Código assembly para LMC

## 1. Somar números digitados até o usuário digitar 0
### **Objetivo**

O programa recebe valores, armazena e soma os números digitados até a entrada do valor 0. Ao final, mostra o resultado da soma.

---
### **Funcionamento**
Primeiro, o programa recebe a entrada inicial e verifica se ela é igual a 0. Se for, imprime o resultado, que inicialmente é 0. Caso não seja, soma a entrada ao valor do resultado e retorna o programa para o início. 

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;2;3;0|15|O programa recebeu a sequência de números e somou até receber o 0, e mostrou o resultado da soma da sequência|
|5;0|5|O programa recebeu somente um valor e recebeu o valor de parada 0, e mostrou o único valor|


## 2. Contar quantos números foram digitados até o usuário digitar -1
### **Objetivo**

O programa recebe vários valores de entrada e mostra na tela a quantidade de valores recebidos até o usuário digitar -1.

---
### **Funcionamento**
O programa recebe o valor inicial e testa para verificar se ele é igual a -1. Para isso, soma o valor com 1; se -1 + 1 = 0, significa que o valor recebido é -1, então o programa mostra o resultado na tela. Caso o valor não seja -1, soma 1 ao contador de números digitados e retorna ao início.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|2;3;5;6;7;-1|5|O programa recebe os valores e foi somando a quantidade até receber o valor de parada -1 e mostrou na tela a quantidade|
|10;-1|1|O programa só recebeu um valor significativo e o valor de parada -1 e mostou na tela a quantidade única do valor recebido|

## 3. Encontrar o menor valor de uma série de números terminada em -1
### **Objetivo**

O programa recebe uma série de números até o valor de parada -1 e mostra na tela o menor valor recebido dessa série.

---
### **Funcionamento**
O programa recebe os números em sequência e verifica se cada entrada é igual a -1. Se for, o programa encerra e mostra o menor valor encontrado. Caso não seja, carrega o número e analisa se ele é menor que o valor armazenado anteriormente. Se for menor, guarda o novo valor como o menor número e retorna o programa para o início.


|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;5;2;1;-1|1|O programa recebeu a série de números, armazena os resultados, sempre procurando o menor valor, quando recebe o valor de parada -1 mostra o menor valor na tela. |
|1;0;2;-1|0|O programa recebeu os valores buscou o menor e mostou na saída depois de receber o valor de parada -1|

## 4. Encontrar o maior valor de uma série de números terminada em -1
### **Objetivo**

O programa recebe um série de números até o valor de parada -1 e mostra na tela o maior valor recebido dessa série.

---
### **Funcionamento**
O programa recebe os números em sequência e verifica se cada entrada é igual a -1. Se for, o programa encerra e mostra o maior valor encontrado. Caso não seja, carrega o número e analisa se ele é maior que o valor armazenado anteriormente. Se for maior, guarda o novo valor como o maior número e retorna o programa para o início.


|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;5;2;1;-1|10|O programa recebeu a série de números, armazena os resultados, sempre procurando o maior valor, quando recebe o valor de parada -1 mostra o maior valor na tela. |
|1;0;2;-1|2|O programa recebeu os valores buscou o maior e mostou na saída depois de receber o valor de parada -1|

## 5. Cálcular a média de uma série terminada em -1
### **Objetivo**

O programa recebe um série de números até o valor de parada -1, soma os valores e mostra a média dos valores recebidos.

---
### **Funcionamento**
O programa recebe uma série de entrada dos números até que o usuário digite -1, que funciona como um valor de sentinela para indicar o final da sequência. Esse valor não é considerado no cálculo da média.
Depois que a entrada termina, o programa possui duas informações principais: a soma de todos os números e a quantidade de números digitados. A média é calculada dividindo a SOMA pela QTD.
Ele subtrai a quantidade de números da soma repetidamente e, a cada subtração realizada, aumenta em 1 o valor da variável MEDIA. Quando não é mais possível realizar outra subtração sem obter um resultado negativo, o valor armazenado em MEDIA representa o resultado inteiro da divisão.


|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;8;7;15;-1|10|O programa recebeu a série de números, armazena os resultados, soma os valores e subtrai pela quantidade de números recebidos. |
|10;2;-1|6|O programa receveu o a série de números, somou os valores 10 e 2 obtendo 12 e dividiu por 2 que foi a quantidade de números recebidos.|

## 6. Contar quantos números positivos e quantos negativos foram digitados em uma série terminada em 0
### **Objetivo**

O programa recebe um série de números até o valor de parada 0, conta separadamente a quantidade de positivos e negativos e mostra os dois valores.

---
### **Funcionamento**
O programa recebe os valores e testa duas condições. Se o valor for 0, o programa para e imprime as quantidades de positivos e negativos, que inicialmente são 0. Caso não seja 0, o programa testa se o valor é positivo. Se for, carrega o contador de positivos e adiciona 1. Caso contrário, o número é negativo, então carrega o contador de negativos e adiciona 1. Depois desses passos, o programa retorna ao

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|1;5;2;-1;-2;-3;0|3;3|O programa recebeu a série de números, conta quantos números positivos e quantos negativos foram digitados, e mostra na tela os dois valores depois do valor de parada 0. |
|1;0;2;-1;-3;-4|2;3|O programa recebeu os valores de uma série os números positivos tinham menor quantidade que os negativos, recebeu o valor de parada 0 e mostrou os valores.|

## 7. Somar apenas os números pares de uma série terminada em -1
### **Objetivo**

O programa recebe uma série terminada em -1, e soma somente os números pares e mostra o resultado.

---
### **Funcionamento**
Primeiro, o programa recebe um valor e testa para verificar se ele é igual a -1. Para isso, soma -1 + 1; se o resultado for 0, o programa para e imprime o valor da soma, que inicialmente é 0, indicando que a série está vazia.

Caso o valor não seja -1, o programa testa se ele é um número par, realizando subtrações sucessivas de 2. Se o valor eventualmente chegar a 0, significa que ele é par. Nesse caso, o valor é armazenado para ser somado aos próximos números pares, e o programa retorna ao início.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;2;1;3|12|O programa recebeu a sequência de números e somou somente os números pares 10 e 2 e mostrou o resultado em tela|
|5;2;3;2;1;2|6|O programa recebeu a sequência de números e somou somente os pares e mostrou o resultado em tela|
