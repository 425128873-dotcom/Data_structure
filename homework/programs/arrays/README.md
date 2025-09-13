#include <stdio.h>

int main() {
    int pares[10];
    int i;
    long long cuenta;
    int ultimoDigito;

    // Pedir el número de cuenta
    printf("Ingrese su numero de cuenta: ");
    scanf("%lld", &cuenta);

    // Generar los primeros 10 números pares
    for (i = 0; i < 10; i++) {
        pares[i] = (i + 1) * 2;  // 2, 4, 6, ..., 20
    }

    // Imprimir en orden inverso
    printf("\nNumeros pares en orden inverso:\n");
    for (i = 9; i >= 0; i--) {
        printf("%d ", pares[i]);
    }
    printf("\n");

    // Calcular el último dígito del número de cuenta
    ultimoDigito = cuenta % 10;

    // Modificar el arreglo en el índice correspondiente
    if (ultimoDigito >= 0 && ultimoDigito < 10) {
        pares[ultimoDigito] = -1;
    }

    // Imprimir arreglo modificado
    printf("\nArreglo modificado:\n");
    for (i = 0; i < 10; i++) {
        printf("%d ", pares[i]);
    }
    printf("\n");

    return 0;
}
