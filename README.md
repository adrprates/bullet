# Funções

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
