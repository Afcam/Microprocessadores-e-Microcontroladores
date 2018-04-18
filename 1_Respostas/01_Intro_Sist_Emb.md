
## 1. O que são sistemas embarcados?
  Um sistema embarcado é um computador construído para o único propósito da sua aplicação, ao invés de um sistema computacional generalizado.
  
## 2. O que são sistemas microprocessados?
  Sao sistemas que possuem um microprocessador que incorpora as funções de uma unidade central de computação (UCP) em um único circuito integrado, ou no máximo alguns circuitos integrados.

## 3. Apresente aplicações de sistemas embarcados:
###  a) Para industria automotiva;
    Injeção Eletronica, GPS, Alarme, Air Bag
  
###  b) Para eletrodomesticos;
    TVs, Geladeira, Microondas, DVD, Maquina de Lavar.
    
###  c) Para automação industrial.
    Robos,Esteiras eletronicas, Controle dos sensores.
  
## 4. Cite arquiteturas possiveis e as diferenças entre ela.
   Temos a arquitetura de Von Neumann que apresenta um barramento externo compartilhado entre dados e endereços. Embora apresente baixo custo, esta arquitetura apresenta desempenho limitado pelo gargalo do barramento.
   Já na arquitetura de Harvard existem dois barramentos externos independentes, e normalmente com memórias independentes,para dados e endereços. Isto reduz de forma sensível o gargalo de barramento.

## 5. Por que usamos MSP430 na disciplina, ao inves de outro microcontrolador ?
 O MSP430 é um processador de 16 bits particularmente direto com arquitetura von Neumann e mais simples do que um processador de 8 bits com endereços de 16 bits.
 
  Outra característica é que ele foi projetado com os compiladores em mente. A maioria dos pequenos microcontroladores agora está programada em C e é importante que um compilador possa produzir um código compacto e eficiente.
  
E tambem o MSP430 é o microcontrolador mais simples do portfólio atual da TI. Seus irmãos mais poderosos incluem o TMS470, baseado no ARM7 de 32/16-bit e no C2000, que incorpora um processador de sinal digital. Vários recursos tornam o MSP430 adequado para aplicações de baixa potência e portáteis:
