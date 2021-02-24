# Cocktail-sort

public static int[] cocktailSort(int[] vetor)

{

    int tamanho, inicio, fim, swap, aux;

    tamanho = vetor.Length;

    inicio = 0;

    fim = tamanho - 1;

    swap = 0;

    while (swap == 0 &amp;&amp; inicio < fim)

    {

        swap = 1;

        for (int i = inicio; i < fim; i = i + 1)

        {

            if (vetor[i] > vetor[i + 1])

            {

                aux = vetor[i];
             vetor[i] = vetor[i + 1];

                vetor[i + 1] = aux;
              swap = 0;

            }

        }

        fim = fim - 1;
 
        for (int i = fim; i > inicio; i = i - 1)
        {

            if (vetor[i] < vetor[i - 1])

            {

                aux = vetor[i];

                vetor[i] = vetor[i - 1];

                vetor[i - 1] = aux;

                swap = 0;

            }

        }

 
        inicio = inicio + 1;

    }
 
    return vetor;

}
