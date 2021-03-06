# **Capítulo 7.4: Loops - Break / Continue**

Por Renata Machado

#### 7.4.1 - Break

O comando **break** é geralmente associado às estruturas de repetição \([for](https://alexsalgado.gitbooks.io/introducao-a-programacao-em-c/content/capitulo-71-for.html), while, [do while](https://alexsalgado.gitbooks.io/introducao-a-programacao-em-c/content/capitulo-7-loops-dowhile.html)\) e ao comando [switch](https://alexsalgado.gitbooks.io/introducao-a-programacao-em-c/content/capitulo-62-tomada-de-decisoes-switch.html) e é utilizado para realizar uma parada imediata do bloco de comando em execução no momento de sua chamada.

Em estruturas de repetição sua função é evitar que o programa continue rodando o laço após ter encontrando a informação que necessitava. Ex:

```c
void busca ( Int v)
{
    int b;
    For (b=0; b<100; b++) {
    Printf (“ o numero eh: %d”, b);
        If (b==v) break; // se b for igual o valor buscado, o programa sairá do FOR e continuará com sua execução
    }
}
```

Já no comando **switch**, sua função é evitar que o programa continue fazendo as verificações caso já tem encontrando a informação desejada:

```c
#include <stdio.h>
#include <conio.h>


int main (void)
{
    intvalor;
    printf("Digite um valor de 1 a 7: ");
    scanf("%d", &valor);
    switch( valor )
    {
        case1 :
            printf("Domingo\n");
        break;
        case2 :
            printf("Segunda\n");
        break;
        case3 :
            printf("Terça\n");
        break;
        case4 :
            printf("Quarta\n");
        break;
        case5 :
            printf("Quinta\n");
        break;
        case6 :
            printf("Sexta\n");
        break;
        case7 :
            printf("Sabado\n");
        break;
        default:
        printf("Valor invalido!\n");
    }

getch();
return 0;
}
```

Assumindo que o valor informado seja 5, o programa rodará até o **case 5**, imprimirá “**Quinta**” e será encerrado.

#### 7.4.2 - Continue

 O comando ** continue** tem função semelhante ao do BREAK \\(forçar uma ação\\) porém está associado apenas às estruturas de repetição, e diferente do break, seu intuito é forçar a próxima iteração do laço a ocorrer, ignorando qualquer instrução que venha depois dele.

  


No exemplo abaixo usamos um **while** para realizar a impressão dos números entre a e b, exceto o número 5. Ao usar o comando continue após a verificação, forçamos o programa a voltar para o início do laço \(while\), pulando o comando de impressão, caso o valor de a seja 5.

 



```c
#include<stdio.h>
#include<stdlib.h>

int main()
{
    int a,b;
    printf("Digite o valor de a:\n");
    scanf("%d",&a);
    printf("Digite o valor de b:\n");
    scanf("%d",&b);
    printf("Os numeros existentes entre eles sao:\n");
    while(a < b){
        a = a + 1;
        if (a==5)
            continue;
        printf("%d\n",a);
    }

system("pause");
return 0;
}
```

```
  A impressão desse programa seria:
```

![](/assets/continue.png)





Referências:

 Os comandos CONTINUE e BREAK: pausando e alterando o fluxo de laços e testes condicionais. _Página eletrônica_.

_&lt;_[_http://www.cprogressivo.net/2013/02/Os-comandos-CONTINUE-e-BREAK--pausando-e-alterando-o-fluxo-de-lacos-e-testes-condicionais.html_](http://www.cprogressivo.net/2013/02/Os-comandos-CONTINUE-e-BREAK--pausando-e-alterando-o-fluxo-de-lacos-e-testes-condicionais.html)_&gt; Acessado em 12 de novembro de 2017._

**CASAVELLA,** Eduardo; O comando continue em C. _Página eletrônica_.

&lt;[http://linguagemc.com.br/o-comando-continue/](http://linguagemc.com.br/o-comando-continue/)&gt;_Acessado em 12 de novembro de 2017._

 

