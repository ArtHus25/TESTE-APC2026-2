# Código assembly para LMC

## 1. Contador Crescente com input duplo
### **Objetivo**

O programa precisa da entrada de dois números, e vai imprimir todos os números desde o primeiro até o último.

---
### **Funcionamento**
Primeiro recebe o input inicial do usuário **(NUM1)** e armazena o valor na memória **(datNUM1)**; recebe o segundo input **(NUM2)** e armazena o valor na memória **(datNUM2)**. Depois o programa entra no loop e carrega o valor de **(NUM1)** e mostra o primeiro número na saida **(OUT)**.
Agora o programa precisa analisar se os números são iguais, então subtrai **(SUB)** os dois valores **(NUM1)** e **(NUM2)**; se o valor for igual a zero **(BRZ)** o programa manda encerrar a execussão **(HLT)**. 
Caso o número ainda não seja igual o programa soma 1 **(ADD)** ao valor de atual **(NUM1 - NUM 2)** e armazena esse resultado em **(datNUM1)** e por fim manda o programa novamente para o loop**(BRA)** e repetir o processo até o final.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10,15|10,11,12,13,14,15|O programa recebe dois valores e mostra o inicial e todos os números até o final|
|5,6|5,6|O programa só recebeu dois valores e mostrou mostrou eles na saída|


## 2. Sequência de Fibonacci
### **Objetivo**

O Programa deve receber um Valor de entrada e mostrar da tela essa quantidade de números da sequência de Fibonacci.

---
### **Funcionamento**
O programa recebe o valor de entrada **(N)** e armazena **(STA)** esse valor na memória. Em seguida, carrega o primeiro valor da sequência de Fibonacci **(FIB1)** e o mostra na saída **(OUT)**. Depois, carrega a variável que controla a posição inicial **(POS)**, adiciona **(ADD)** 1 e armazena o novo valor da posição **(STA)**. O segundo valor da sequência **(FIB2)** também é carregado e mostrado na saída **(OUT)**. A posição é novamente incrementada **(ADD)** em 1 e armazenada**(STA)**.

Em seguida, o programa soma o primeiro valor **(FIB1)** com o segundo **(FIB2)** e armazena o resultado em uma terceira variável **(FIB)**, que também é mostrada na saída **(OUT)**. Depois, a posição atual **(POS)** é carregada, incrementada**(ADD)** em 1 e armazenada**(STA)** novamente.

Para manter a sequência de Fibonacci, o valor de **(FIB2)** é armazenado em FIB1, enquanto o resultado da soma **(FIB)** é armazenado em **(FIB2)**. Dessa forma, os dois valores são atualizados para realizar as próximas somas.

Por fim, o programa utiliza um loop com uma condicional para imprimir a quantidade de números definida pelo valor de entrada **(N)**. A posição **(POS)** é subtraída **(SUB)** do valor de entrada **(N)** e, enquanto o resultado for positivo **(BRP)**, o programa retorna para a soma dos novos valores de **(FIB1)** e **(FIB2)**. A cada número impresso, a posição é incrementada em 1. Quando POS atinge o valor de entrada N, a condição deixa de ser atendida e o programa é finalizado.**(HLT)**

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|4|0,1,1,2 e 3|O programa recebe um valor N e mostra os N números da sequência de Fibonacci|
|0|0,1 e 1|O programa sempre mostra os doís valores iniciais da sequência de Fibonacci|

## 3. Multiplicação de dois números
### **Objetivo**

O programa recebe a entrade de dois números e deve imprimir o resultado da multiplicação

---
### **Funcionamento**

O programa recebe os valores iniciais **(NUM1)** e **(NUM2)** e armazena **(STA)** ambos. Para multiplicarmos um números usamos uma soma **(ADD)** sucessiva do primeiro valor **(NUM1)** por ele mesmo igual ao valor da segunda entrada **(NUM2)**.

Primeiramente, o programa verifica o segundo valor **(NUM2)** por meio de uma condicional. Se ele for igual a 0 **(BRZ)**, o programa carrega **(LDA)** a variável **(RESULTADO)**, que possui o valor inicial 0. Caso contrário, o programa carrega o primeiro valor **(NUM1)**, realiza a soma **(ADD)** com **(RESULTADO)** e armazena **(STA)** o novo resultado.

Em seguida, o programa carrega **(NUM2)** novamente utilizando **(LDA)**, subtrai **(SUB)** 1 e armazena **(STA)** o novo valor. Depois, entra em um loop por meio de **(BRA)**, retornando para verificar novamente o valor de **(NUM2)**. Esse processo de soma sucessiva continua até que **(NUM2)** chegue a 0, imprimendo o valor do resultado e encerrando o programa.

|ENTRADA|SAÍDA|EXPLICAÇÃO|
|:--|:--:|:--:|
|10,2|20|O programa recebe um valor N e mostra os N1 e faz um soma sucessiva vezes igual a N2 e mostra o resultado |
|2,0|0|O programa recebe o valor N1, mas ao receber N2=0 mostra o resultado 0 para respeitar a regra da multiplicação|
