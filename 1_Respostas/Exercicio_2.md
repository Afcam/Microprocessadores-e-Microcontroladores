## 1. Quais as diferenças entre os barramentos de dados e de endereços?
  O barramento de dados serve para escrever ou ler um determinado dado na memoria,
enquanto o de endereços serve para indicar o local da memoria que sera utilizado.

## 2. Quais são as diferenças entre as memórias RAM e ROM?
  A memoria RAM é uma memória reconfiguravel que pode ser tanto lida e escrita, mas perdese os dados quando é desligada.
Já a memoria ROM é uma memoria que apenas poderá ser escrita uma unica vez e apenas lida. 

## 3. Considere o código abaixo:

```C
#include <stdio.h>
int main(void)
{
	int i;
	printf("Insira um número inteiro: ");
	scanf("%d", &i);
	if(i%2)
		printf("%d eh impar.\n");
	else
		printf("%d eh par.\n");
	return 0;
}
```

Para este código, responda:
#### (a) A variável `i` é armazenada na memória RAM ou ROM? Por quê? 
  É armazenada na meoria RAM, pois é um probrama que irá perder os dados quando for finalizado.
#### (b) O programa compilado a partir deste código é armazenado na memória RAM ou ROM? Por quê?
  O programa fica na memoria ROM, uma vez que fica salvo mesmo apos se desligar a maquina.

## 4. Quais são as diferenças, vantagens e desvantagens das arquiteturas Harvard e Von Neumann?
  ###### Von Neumann
    * Arquitetura mais simples
    * Mais lento pois nao permite acesso simultãneo ás memórias.
    * Geralmente é CISC
  ###### Havard
    * Arquitetura mais complexa
    * Mais rápido, pois permite acesso simultãneo ás memórias.
    * Geralmente é RISC
    * permite Pipelining
    
## 5. Considere a variável inteira `i`, armazenando o valor `0x8051ABCD`. Se `i` é armazenada na memória a partir do endereço `0x0200`, 
como ficam este byte e os seguintes, considerando que a memória é:
#### (a) Little-endian;
* CD -> 0x0200
* AB -> 0x0200 + 1
* 51 -> 0x0200 + 2
* 80 -> 0x0200 + 3
#### (b) Big-endian.
* 80 -> 0x0200
* 51 -> 0x0200 + 1
* AB -> 0x0200 + 2
* CD -> 0x0200 + 3

## 6. Sabendo que o processador do MSP430 tem registradores de 16 bits, como ele soma duas variáveis de 32 bits?

Ele guarda na memoria  RAM as variaveis de 32bits, necessitando de 2 ciclos para cada. Depois acessa as variaveis da memoria somando o LSB de cada, guradandando o resultado tambem na memoria e finaliza somando o MSB das duas variaveis.


