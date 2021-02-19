Exercícios em C
================
Miguel Angelo
19/02/2021

Este repositório foi feito para publicar exercícios das aulas de
programação em C

## Exercícios

Converta Real em Dolar:

``` c
#include <stdio.h>
#include <stdlib.h>
int main(int argc, char *argv[]) {
  printf("Conversor de Moeda - Real/Dolar\n");
  printf("\nInsira um valor em Reais: ");
  float real, conversao, txc; //txc é a taxa comercial
  txc = 5.53;
  scanf("%f", &real);
  conversao = real / txc;
  printf ("\nA conversão de real para dolar: %.2f", conversao);
  return 0;
}
```

Converta Celsius para Kelvin:

``` c
#include <stdio.h>
#include <stdlib.h>
int main(int argc, char *argv[]) {
  printf("Conversor de Temperatura - Celsius/Kelvin\n");
  printf("\nInsira uma temperatura em graus Celsius: ");
  float cel, kel;
  scanf("%f", &cel);
  kel = cel + 273; //fórmula de conversão °C para °K
  printf ("\nEsta temperatura corresponde em graus Kelvin à: %.2f", kel);
  return 0;
}
```

Calcule o comprimento de uma circunferência:

``` c
#include <stdio.h>
#include <stdlib.h>
int main(int argc, char *argv[]) {
  printf("Calcular o comprimento de uma circunferencia\n");
  printf("\nInsira um valor para o raio: ");
  float raio, pi, comprimento;
  pi = 3.14;
  scanf("%f", &raio);
  comprimento = 2 * raio * pi;
  printf ("\nO comprimento da circunferencia é: %.2f", comprimento);
  return 0;
}
```

Calcule a Área de uma circunferência:

``` c
#include <stdio.h>
#include <stdlib.h>
int main(int argc, char *argv[]) {
  printf("Calcular a Área de uma circunferencia\n");
  printf("\nInsira o valor do raio: ");
  float raio, pi, area;
  pi = 3.14;
  scanf("%f", &raio);
  area = pi * (raio * raio);
  printf ("\nA área da circunferencia é: %.2f", area);
  return 0;
}
```

Receba a taxa de correção do salário mínimo, e devolva o valor ja com o
aumento:

``` c
#include <stdio.h>
#include <stdlib.h>
int main(int argc, char *argv[]) {
  printf("Descubra o valor do salário mínimo com aumento\n");
  printf("\nInsira a taxa de correção: ");
  float slm, pct, txc, vlr;
  /*slm = salário mínimo; pct = valor da porcentagem da taxa de correção (5% -> 5); 
  txc = valor em decimal da taxa de correção (5 -> 0,05); vlr = valor total com aumento*/
  slm = 1100;
  scanf("%f", &pct);
  txc = pct / 100;
  vlr = slm * txc + slm;
  printf ("\nO salário mínimo agora é: %.2f", vlr);
  return 0;
}
```

Transforme uma letra minúscula em maiúscula:

``` c
#include <stdlib.h>
#include <stdio.h>
int main(int argc, char *argv[]){
    printf("Transforme a letra de minúscula para maiúscula: \n");
    printf("\nInsira uma letra: ");
    char m, M;
    scanf("%c", &m);
    M = m - 32; 
    //diferença de 32 entre as letras maiúsculas e minúsculas na tabela ASCII
    printf("\nSua letra em maiúsculo é: %c", M);
    return 0;
}
```

Calcule o IMC de uma pessoa:

``` c
#include <stdlib.h>
#include <stdio.h>
int main(){
    printf("Calcule o IMC\n");
    float peso, altura, imc;
    printf("\nInsira o peso: ");
    scanf("%f", &peso);
    printf("\nInsira a altura: ");
    scanf("%f", &altura);
    imc = peso / (altura * altura);
    printf("\nIMC é igual a: %2.f", imc);
    return 0;
}
```

Pela nota do aluno, diga se ele foi aprovado (precisa de 7 pra passar):

``` c
#include <stdlib.h>
#include <stdio.h>
int main(){
    printf("Saiba se você foi aprovado");
    float x;
    printf("\nInsira sua nota: ");
    scanf("%f", &x);
    if(x >= 7){
        printf("Parabéns, você foi aprovado");
    } else{
        printf("Você foi reprovado");
    }
    return 0;
}
```

Saiba se um número é ímpar ou par:

``` c
#include <stdlib.h>
#include <stdio.h>
int main(){
    printf("Saiba se o número é ímpar ou par");
    int x;
    printf("\nInsira um número: ");
    scanf("%d", &x);
    if(x % 2 == 0){
        printf("Seu número é par");
    } else{
        printf("Seu número é ímpar");
    }
    return 0;
}
```

Descubra se um número é múltiplo do outro:

``` c
#include <stdlib.h>
#include <stdio.h>
int main(){
    printf("Saiba se um número é múltiplo do outro");
    int x, y;
    printf("\nInsira um número: ");
    scanf("%d", &x);
    printf("\nInsira o possível múltiplo: ");
    scanf("%d", &y);
    if(x % y == 0){
        printf("%d é múltipo de %d\n", y, x);
    } else{
        printf("%d não é múltipo de %d\n", y, x);
    }
    return 0;
}
```

Dos 5 números inseridos mostre qual o maior e o menor:

``` c
#include <stdlib.h>
#include <stdio.h>
int main(){
    printf("Insira 5 números e descubra qual é o maior e o menor");
    printf("\ninsira 5 números: ");
    int a, b, c, d, e, x;
    scanf("%d %d %d %d %d", &a, &b, &c, &d, &e);
    if (a > b) {
        x = b;
        b = a;
        a = x;
    }
    if (a > c) {
        x = c;
        c = a;
        a = x;
    }
    if (a > d) {
        x = d;
        d = a;
        a = x;
    }
    if (a > e) {
        x = e;
        e = a;
        a = x;
    }
    if (b > c) {
        x = c;
        c = b;
        b = x;
    }
    if (b > d) {
        x = d;
        d = b;
        b = x;
    }
    if (b > e) {
        x = e;
        e = b;
        b = x;
    }
    if (c > d) {
        x = d;
        d = c;
        c = x;
    }
    if (c > e) {
        x = e;
        e = c;
        c = x;
    }
    if (d > e) {
        x = e;
        e = d;
        d = x;
    }
    printf("O maior número é %d e o menor %d", e, a);
    return 0;
}
```
