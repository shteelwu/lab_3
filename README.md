```c
#include <stdio.h>
#include <math.h>

int c(int p) {
    if (p <= 2) {
        return pow(2, p);
    }
    int numbers = pow(2, p) - (p - 2);
    return numbers;
}
int main() {
    int p;
    printf("Введіть кількість розрядів (p): ");
    scanf("%d", &p);

    if (p < 1 || p > 30) {
        printf("Кількість розрядів має бути від 1 до 30\n");
        return 1;
    }

    int result = c(p);
    printf("Кількість %d-розрядних чисел, де три однакові цифри не стоять поруч: %d\n", p, result);

    return 0;
}
