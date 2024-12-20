# Funções

<br>

## Método para imprimir a subárvore esquerda

```cpp
void printLeftSubtree() {
    if (root == NULL || root->left == NULL) {
        printf("Subárvore esquerda está vazia\n");
        return;
    }
    inOrder(root->left); 
    printf("\n");
}
```
<br>

## Método para imprimir a subárvore direita

```cpp
void printRightSubtree() {
    if (root == NULL || root->right == NULL) {
        printf("Subárvore direita está vazia\n");
        return;
    }
    inOrder(root->right); 
    printf("\n");
}
```

<br>

## Método para imprimir apenas os ímpares

```cpp
void printOdds(Node *aux) {
    if (aux == NULL) return; 
    printOdds(aux->left);    
    if (aux->value % 2 != 0) 
        printf("%d ", aux->value);
    printOdds(aux->right);  
}

void printOdds() {
    printf("Números ímpares: ");
    printOdds(root);
    printf("\n");
}
```

<br>

## Método para imprimir apenas os pares

```cpp
void printEvens(Node *aux) {
    if (aux == NULL) return; 
    printEvens(aux->left);   
    if (aux->value % 2 == 0) 
        printf("%d ", aux->value);
    printEvens(aux->right);  
}

void printEvens() {
    printf("Números pares: ");
    printEvens(root);
    printf("\n");
}

```
