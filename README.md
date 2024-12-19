# Funções

<br>

## Método para imprimir a subárvore esquerda

```cpp
void printLeftSubtree() {
    if (root == NULL || root->left == NULL) {
        printf("Subárvore esquerda está vazia\n");
        return;
    }
    inOrder(root->left); // Reutiliza a lógica do inOrder para percorrer a subárvore esquerda
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
    inOrder(root->right); // Reutiliza a lógica do inOrder para percorrer a subárvore direita
    printf("\n");
}
```

<br>

## Método para imprimir apenas os ímpares

```cpp
void printOdds(Node *aux) {
    if (aux == NULL) return; // Caso base: nó nulo
    printOdds(aux->left);    // Percorre a subárvore esquerda
    if (aux->value % 2 != 0) // Verifica se é ímpar
        printf("%d ", aux->value);
    printOdds(aux->right);   // Percorre a subárvore direita
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
    if (aux == NULL) return; // Caso base: nó nulo
    printEvens(aux->left);   // Percorre a subárvore esquerda
    if (aux->value % 2 == 0) // Verifica se é par
        printf("%d ", aux->value);
    printEvens(aux->right);  // Percorre a subárvore direita
}

void printEvens() {
    printf("Números pares: ");
    printEvens(root);
    printf("\n");
}

```
