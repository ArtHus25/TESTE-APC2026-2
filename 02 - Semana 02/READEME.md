# Código assembly para LMC

## Contador Crescente com input duplo
### **Objetivo**

O programa precisa da entrada de dois números, e vai imprimir todos os números desde o primeiro até o último.

---
### **Funcionamento**
Primeiro recebe o input inicial do usuário **(NUM1)** e armazena o valor na memória **(datNUM1)**; recebe o segundo input **(NUM2)** e armazena o valor na memória **(datNUM2)**. Depois o programa entra no loop e carrega o valor de **(NUM1)** e mostra o primeiro número na saida **(OUT)**.
Agora o programa precisa analisar se os números são iguais, então subtrai **(SUB)** os dois valores **(NUM1)** e **(NUM2)**; se o valor for igual a zero **(BRZ)** o programa manda encerrar a execussão **(HLT)**. 
Caso o número ainda não seja igual o programa soma 1 **(ADD)** ao valor de atual **(NUM1 - NUM 2)** e armazena esse resultado em **(datNUM1)** e por fim manda o programa novamente para o loop**(BRA)** e repetir o processo até o final.
