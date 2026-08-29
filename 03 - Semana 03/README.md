# Código assembly para LMC

## 1. Somar números digitados até o usuário digitar 0
### **Objetivo**

O programa recebe valores, armazena e soma e mostra o resultado da soma dos números digitados até o entrada do valor 0.

---
### **Funcionamento**
Primeiro recebe o input inicial do usuário **(NUM1)** e armazena o valor na memória **(datNUM1)**; recebe o segundo input **(NUM2)** e armazena o valor na memória **(datNUM2)**. Depois o programa entra no loop e carrega o valor de **(NUM1)** e mostra o primeiro número na saida **(OUT)**.
Agora o programa precisa analisar se os números são iguais, então subtrai **(SUB)** os dois valores **(NUM1)** e **(NUM2)**; se o valor for igual a zero **(BRZ)** o programa manda encerrar a execussão **(HLT)**. 
Caso o número ainda não seja igual o programa soma 1 **(ADD)** ao valor de atual **(NUM1 - NUM 2)** e armazena esse resultado em **(datNUM1)** e por fim manda o programa novamente para o loop**(BRA)** e repetir o processo até o final.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;2;3;0|15|O programa recebeu a sequência de números e somou até receber o 0, e mostrou o resultado da soma da sequência|
|5;0|5|O programa recebeu somente um valor e recebeu o valor de parada 0, e mostrou o único valor|


## 2. Contar quantos números foram digitados até o usuário digitar -1
### **Objetivo**

O Programa recebe vários valores de entrada e imprime em tela a quantidade valores foram recebidos até o receber -1.

---
### **Funcionamento**
O programa recebe o valor de entrada **(N)** e armazena **(STA)** esse valor na memória. Em seguida, carrega o primeiro valor da sequência de Fibonacci **(FIB1)** e o mostra na saída **(OUT)**. Depois, carrega a variável que controla a posição inicial **(POS)**, adiciona **(ADD)** 1 e armazena o novo valor da posição **(STA)**. O segundo valor da sequência **(FIB2)** também é carregado e mostrado na saída **(OUT)**. A posição é novamente incrementada **(ADD)** em 1 e armazenada**(STA)**.

Em seguida, o programa soma o primeiro valor **(FIB1)** com o segundo **(FIB2)** e armazena o resultado em uma terceira variável **(FIB)**, que também é mostrada na saída **(OUT)**. Depois, a posição atual **(POS)** é carregada, incrementada**(ADD)** em 1 e armazenada**(STA)** novamente.

Para manter a sequência de Fibonacci, o valor de **(FIB2)** é armazenado em FIB1, enquanto o resultado da soma **(FIB)** é armazenado em **(FIB2)**. Dessa forma, os dois valores são atualizados para realizar as próximas somas.

Por fim, o programa utiliza um loop com uma condicional para imprimir a quantidade de números definida pelo valor de entrada **(N)**. A posição **(POS)** é subtraída **(SUB)** do valor de entrada **(N)** e, enquanto o resultado for positivo **(BRP)**, o programa retorna para a soma dos novos valores de **(FIB1)** e **(FIB2)**. A cada número impresso, a posição é incrementada em 1. Quando POS atinge o valor de entrada N, a condição deixa de ser atendida e o programa é finalizado.**(HLT)**

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|2;3;5;6;7;-1|5|O programa recebe os valores e foi somando a quantidade até receber o valor de parada -1 e mostrou na tela a quantidade|
|10;-1|1|O programa só recebeu um valor significativo e o valor de parada -1 e mostou na tela a quantidade única do valor recebido|

## 3. Encontrar o menor valor de uma série de números terminada em -1
### **Objetivo**

O programa recebe um série de números até o valor de parada -1 e mostra na tela o menor valor recebido dessa série

---
### **Funcionamento**

O programa recebe os valores iniciais **(NUM1)** e **(NUM2)** e armazena **(STA)** ambos. Para multiplicarmos um números usamos uma soma **(ADD)** sucessiva do primeiro valor **(NUM1)** por ele mesmo igual ao valor da segunda entrada **(NUM2)**.

Primeiramente, o programa verifica o segundo valor **(NUM2)** por meio de uma condicional. Se ele for igual a 0 **(BRZ)**, o programa carrega **(LDA)** a variável **(RESULTADO)**, que possui o valor inicial 0. Caso contrário, o programa carrega o primeiro valor **(NUM1)**, realiza a soma **(ADD)** com **(RESULTADO)** e armazena **(STA)** o novo resultado.

Em seguida, o programa carrega **(NUM2)** novamente utilizando **(LDA)**, subtrai **(SUB)** 1 e armazena **(STA)** o novo valor. Depois, entra em um loop por meio de **(BRA)**, retornando para verificar novamente o valor de **(NUM2)**. Esse processo de soma sucessiva continua até que **(NUM2)** chegue a 0, imprimendo o valor do resultado e encerrando o programa.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;5;2;1;-1|1|O programa recebeu a série de números, armazena os resultados, sempre procurando o menor valor, quando recebe o valor de parada -1 mostra o menor valor na tela. |
|1;0;2;-1|0|O programa recebeu os valores buscou o menor e mostou na saída depois de receber o valor de parada -1|

## 4. Encontrar o maior valor de uma série de números terminada em -1
### **Objetivo**

O programa recebe um série de números até o valor de parada -1 e mostra na tela o maior valor recebido dessa série.

---
### **Funcionamento**

O programa recebe os valores iniciais **(NUM1)** e **(NUM2)** e armazena **(STA)** ambos. Para multiplicarmos um números usamos uma soma **(ADD)** sucessiva do primeiro valor **(NUM1)** por ele mesmo igual ao valor da segunda entrada **(NUM2)**.

Primeiramente, o programa verifica o segundo valor **(NUM2)** por meio de uma condicional. Se ele for igual a 0 **(BRZ)**, o programa carrega **(LDA)** a variável **(RESULTADO)**, que possui o valor inicial 0. Caso contrário, o programa carrega o primeiro valor **(NUM1)**, realiza a soma **(ADD)** com **(RESULTADO)** e armazena **(STA)** o novo resultado.

Em seguida, o programa carrega **(NUM2)** novamente utilizando **(LDA)**, subtrai **(SUB)** 1 e armazena **(STA)** o novo valor. Depois, entra em um loop por meio de **(BRA)**, retornando para verificar novamente o valor de **(NUM2)**. Esse processo de soma sucessiva continua até que **(NUM2)** chegue a 0, imprimendo o valor do resultado e encerrando o programa.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;5;2;1;-1|10|O programa recebeu a série de números, armazena os resultados, sempre procurando o maior valor, quando recebe o valor de parada -1 mostra o maior valor na tela. |
|1;0;2;-1|2|O programa recebeu os valores buscou o maior e mostou na saída depois de receber o valor de parada -1|

## 5. Cálcular a média de uma série terminada em -1
### **Objetivo**

O programa recebe um série de números até o valor de parada -1, soma os valores e mostra a média dos valores recebidos.

---
### **Funcionamento**

O programa recebe os valores iniciais **(NUM1)** e **(NUM2)** e armazena **(STA)** ambos. Para multiplicarmos um números usamos uma soma **(ADD)** sucessiva do primeiro valor **(NUM1)** por ele mesmo igual ao valor da segunda entrada **(NUM2)**.

Primeiramente, o programa verifica o segundo valor **(NUM2)** por meio de uma condicional. Se ele for igual a 0 **(BRZ)**, o programa carrega **(LDA)** a variável **(RESULTADO)**, que possui o valor inicial 0. Caso contrário, o programa carrega o primeiro valor **(NUM1)**, realiza a soma **(ADD)** com **(RESULTADO)** e armazena **(STA)** o novo resultado.

Em seguida, o programa carrega **(NUM2)** novamente utilizando **(LDA)**, subtrai **(SUB)** 1 e armazena **(STA)** o novo valor. Depois, entra em um loop por meio de **(BRA)**, retornando para verificar novamente o valor de **(NUM2)**. Esse processo de soma sucessiva continua até que **(NUM2)** chegue a 0, imprimendo o valor do resultado e encerrando o programa.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10;5;2;1;-1|1|O programa recebeu a série de números, armazena os resultados, sempre procurando o menor valor, quando recebe o valor de parada -1 mostra o menor valor na tela. |
|1;0;2;-1|0|O programa recebeu os valores buscou o menor e mostou na saída depois de receber o valor de parada -1|

## 6. Contar quantos números positivos e quantos negativos foram digitados em uma série terminada em 0
### **Objetivo**

O programa recebe um série de números até o valor de parada 0, conta separadamente a quantidade de positivos e negativos e mostra os dois valores.

---
### **Funcionamento**

O programa recebe os valores iniciais **(NUM1)** e **(NUM2)** e armazena **(STA)** ambos. Para multiplicarmos um números usamos uma soma **(ADD)** sucessiva do primeiro valor **(NUM1)** por ele mesmo igual ao valor da segunda entrada **(NUM2)**.

Primeiramente, o programa verifica o segundo valor **(NUM2)** por meio de uma condicional. Se ele for igual a 0 **(BRZ)**, o programa carrega **(LDA)** a variável **(RESULTADO)**, que possui o valor inicial 0. Caso contrário, o programa carrega o primeiro valor **(NUM1)**, realiza a soma **(ADD)** com **(RESULTADO)** e armazena **(STA)** o novo resultado.

Em seguida, o programa carrega **(NUM2)** novamente utilizando **(LDA)**, subtrai **(SUB)** 1 e armazena **(STA)** o novo valor. Depois, entra em um loop por meio de **(BRA)**, retornando para verificar novamente o valor de **(NUM2)**. Esse processo de soma sucessiva continua até que **(NUM2)** chegue a 0, imprimendo o valor do resultado e encerrando o programa.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|1;5;2;-1;-2;-3;0|3;3|O programa recebeu a série de números, conta quantos números positivos e quantos negativos foram digitados, e mostra na tela os dois valores depois do valor de parada 0. |
|1;0;2;-1;-3;-4|2;3|O programa recebeu os valores de uma série os números positivos tinham menor quantidade que os negativos, recebeu o valor de parada 0 e mostrou os valores.|
