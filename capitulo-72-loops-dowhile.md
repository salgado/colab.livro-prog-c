# **Capítulo 7.2: Loops - do..while** {#capítulo-51-entrada-e-saída-de-dadosprintf}

##### **Autor: **Diego Maciel

O comando **do-while **permite que um certo trecho de programa seja executado **ENQUANTO **uma certa condição for **verdadeira**. 

A forma de escrita do comando **do-while **é a seguinte:

> > do  
> >   
> > {
> >
> >   
> > // comandos a serem repetidos
> >
> >   
> > } while \(condição\)  
> > ;  
> > // comandos após o 'do-while'

O funcionamento é o seguinte:

1. Executa os comando dentro do bloco **do-while**;
2. Testa a condição;
3. Se a **condição **for **falsa, **então executa o comando que está logo após o bloco subordinado ao **do-while**.
4. Se **condição** for **verdadeira, **então volta ao passo 1.

O comando **do-while **deve ser usado sempre que:

* **não soubermos exatamente quantas vezes o laço deve ser repetido**;
* o teste deva ser feito **depois da execução **de um bloco de comandos;
* o bloco de comandos deve se **executado pelo menos 1 vez;**

### Exemplos

```cpp
int continua, contador;

contador = 0; 

// nao precisamos inicializar a variável 'continua' pois o teste é feito 
// depois

do 
{
// comandos a serem repetidos

   printf("Repentindo....\n");

   contador = contador + 1;

   printf("Tecle 's' se deseja continuar\n");
   continua = getch();
} while (continua == 's') 

printf("O bloco foi repetido %d vezes", contador);
```

---

```cpp
// Programa que calcula a idade média de um grupo de pessoas
// A finalização da entrada de números é dada por um -1
int soma, quantidade, idade;
float media;
soma = 0;
quantidade = 0;
do {
     printf("Idade da pessoa %d. (tecle -1 se quiser encerrar).\n",
               quantidade+1);
     scanf("%d", &idade);
if (idade > =0)
{
soma = soma + idade;
quantidade = quantidade + 1;
}
} while (idade != -1);
// Faz o calculo da media de idade
if (quantidade > 0)
{
   media = (float) soma / quantidade;
   printf("A media de idade das %d pessoas eh: %5.2f", quantidade,
            media);
}
else printf("Nenhum dado foi informado.");
```



### Referências

Os laços while e do ... while - Aspectos básicos - parte 2 Disponível em &lt; [http://stoa.usp.br/ccpp/weblog/7814.html](http://stoa.usp.br/ccpp/weblog/7814.html)&gt; Acessado e: 14.Nov.2017

SAR_ROGLIA, Márcio; Programação em C++ - Comandos de Repetição Disponível em &lt;_[http://www.inf.pucrs.br/~pinho/LaproI/ComandosDeRepeticao/Repeticao.html](http://www.inf.pucrs.br/~pinho/LaproI/ComandosDeRepeticao/Repeticao.html)_&gt;. Acessado em 14. Nov. 2017._

