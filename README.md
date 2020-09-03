# L-gica-de-Programa-o-em-C
Algoritmos em C envolvendo conhecimento básico de programação

#include <stdio.h>
#include <math.h>

/* Faça um programa que receba diversos números positivos, finalizando com a entrada de um número negativo. Calcule e mostre ao final:
a) A soma de todos os números digitados; b) A quantidade de números digitados;
c) A média dos números digitados;
d) O maior número digitado;
e) O menor número digitado;
f) A média dos números pares digitados;
g) A porcentagem de números ímpares digitados;
*/

int main ()
{

    int n = 0;
    int soma = 0;
    int cont = 0;
    float media = 0;
    int maior = 0;
    int menor = 0;
    int par = 0;
    int somar_par = 0;
    float impar = 0;

    scanf("%d", &n);

    maior = n; /*A variavel "maior" recebe o valor do numero digitado" */
    menor = n; /*A variavel "menor" recebe o valor do numero digitado" */

    while(n > 0)
    {
        cont++; /*A variavel "cont" para contabilizar cada vez que um numero for digitado */
        soma = n + soma;

        if(n > maior) /* A condicao verifica se o numero digitado é maior que a variavel maior */
        {
            maior = n; /* Se a condicao for verdadeira, maior recebe novo valor que é o numero digitado */
        }
        if(n < menor) /* A condicao verifica se o numero digitado é maior que a variavel maior */
        {
            menor =  n; /* Se a condicao for verdadeira, menor recebe novo valor que é o numero digitado */
        }
        if((n%2) == 0) /* A condicao verifica se o o resto da divisão é zero, caso for, o número é par */
        {
            par++;
            somar_par = n + somar_par;
        }
        else /* Caso não for verdadeira */
        {
            impar++;
        }
        scanf("%d", &n); /*Novo valor*/
    }
    printf("\nA soma dos valores digitados: %d", soma);
    printf("\nA quantidade de valores digitados: %d", cont);
    printf("\nA media dos numeros digitados: %.2f", media, (media = soma/cont));
    printf("\nO maior numero digitado: %d", maior);
    printf("\nO menor numero digitado: %d", menor);
    printf("\nA media dos numeros pares digitados: %d", somar_par, (somar_par = somar_par/par));
    printf("\nA porcentagem dos numeros impares digitados: %.2f ", impar, (impar = (impar/100)*cont));

}
