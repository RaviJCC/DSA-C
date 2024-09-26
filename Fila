#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <stdbool.h>
#define TAM 5

typedef struct {
    int id;
    int *elementos;
}  Lista;

Lista* criarLista() {
   Lista *nova = (Lista*)malloc(sizeof(Lista));
   if(nova == NULL){
       printf("sem espaco\n");
       return NULL;
   }
   nova->id = 0;
   nova->elementos = (int*)malloc(sizeof(int)*TAM);
   if(nova->elementos == NULL){
       printf("sem espaco\n");
       free(nova);
       return NULL;
   }
   return nova;
} 


int inserirElemento(Lista *lista, int valor) {
    if(lista == NULL){
       printf("lista nao foi criada\n");
       return 0;
    }

    if(lista->id < TAM) {
       lista->elementos[lista->id] = valor;
       ++(lista->id);
    } else {
        printf("Sem espaco\n");
        return 0;
    }
    return 1;
}

void imprimirElementos(Lista *lista){
     if (lista == NULL) {
         printf("A lista nao foi criada\n");
         return ;
     } 
     
     if(lista->id == 0) {
        printf("A lista esta vazia\n");
        return ;
     }
    
    for(int i = 0; i < lista->id; ++i) {
        printf("%d ", lista->elementos[i]);
    }
    printf("\n");
}


int main() {
    Lista *lista = NULL;
    imprimirElementos(lista);
    
    lista = criarLista();
    imprimirElementos(lista);
    inserirElemento(lista, 7);
    imprimirElementos(lista);
    inserirElemento(lista, 3);
    imprimirElementos(lista);
    inserirElemento(lista, 2);
    imprimirElementos(lista);
    inserirElemento(lista, 6);
    imprimirElementos(lista);
    inserirElemento(lista, 5);
    imprimirElementos(lista);
    inserirElemento(lista, 9); // limite de 5 elementos atingido //
    imprimirElementos(lista);


    return 0;
}
