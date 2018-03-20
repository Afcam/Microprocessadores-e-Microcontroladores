## 1. Dada uma variável a do tipo char (um byte), escreva os trechos de código em C para:
### (a) Somente setar o bit menos significativo de a.
```C
#include <msp430g2553.h>

void main( void )
{
  char A;
  A |= BIT0;          //Seta o Bit 0 para 1
}
```

### (b) Somente setar dois bits de a: o menos significativo e o segundo menos significativo.
```C
#include <msp430g2553.h>

void main( void )
{
  char A;
  A|= BIT0 + BIT1;          //Seta o Bit 0 e 1 para 1
}
```
### (c) Somente zerar o terceiro bit menos significativo de a.
```C
#include <msp430g2553.h>

void main( void )
{
  char A;
  A&= ~BIT2;          //Seta o Bit 3 para 0
}
```
### (d) Somente zerar o terceiro e o quarto bits menos significativo de a.
```C
#include <msp430g2553.h>

void main( void )
{
  char A;
  A &= ~(BIT2 + BIT0);          //Seta o Bit 3 e 4 para 0
}
```
### (e) Somente inverter o bit mais significativo de a.
```C
#include <msp430g2553.h>

void main( void )
{
  char A;
  A ^= ~BIT2;
}
```
### (f) Inverter o nibble mais significativo de a, e setar o nibble menos significativo de a.
<!-- ```C
#include <msp430g2553.h>

void main( void )
{

}
``` -->
## 2. Considerando a placa Launchpad do MSP430, escreva o código em C para piscar os dois LEDs ininterruptamente.
```C
//Piscas Leds
#include <msp430g2553.h>

int main(void)
{
  volatile int i;
  // stop watchdog timer
  WDTCTL = WDTPW | WDTHOLD;
  //Seta o Bit 0 e 6  como Saida
  P1DIR = BIT0 + BIT6;
  // Seta o Bit 0 e 6 de P1 para 0
  P1OUT = 0x00;

  // loop forever
  for (;;) {
    // Liga e desliga o Led
    P1OUT ^= BIT0 + BIT6 ;
    // Atraso
    for (i = 0; i < 0x6000; i++);
  }
}
```

## 3. Considerando a placa Launchpad do MSP430, escreva o código em C para piscar duas vezes os dois LEDs sempre que o usuário pressionar o botão.

## 4. Considerando a placa Launchpad do MSP430, faça uma função em C que pisca os dois LEDs uma vez.
```C
//Piscas Leds
#include <msp430g2553.h>

int main(void)
{
  volatile int i;
  // stop watchdog timer
  WDTCTL = WDTPW | WDTHOLD;
  //Seta o Bit 0 e 6  como Saida
  P1DIR = BIT0 + BIT6;
  // Seta o Bit 0 e 6 de P1 para 0
  P1OUT = 0x00;

  // Liga e desliga o Led
  P1OUT ^= BIT0 + BIT6 ;
  // Atraso
  for (i = 0; i < 0x6000; i++);
  P1OUT ^= BIT0 + BIT6 ;
}
```

## 5. Reescreva o código da questão 2 usando a função da questão 4.

## 6. Reescreva o código da questão 3 usando a função da questão 4.
