# C-
#include <stdio.h>

int main() {
    int n, id, arr[100], i;

    printf("상품 개수를 입력하세요: ");
    scanf_s("%d", &n);

    printf("%d개의 상품 입고수량을 입력하세요:\n", n);
    for (i = 0; i < n; i++) {
        scanf_s("%d", &arr[i]);
    }

    printf("%d개의 상품 판매수량을 입력하세요:\n", n);
    for (i = 0; i < n; i++) {
        int sold;
        scanf_s("%d", &sold);
        arr[i] -= sold;   
    }

    printf("조회할 상품 ID를 입력하세요 (1 ~ %d): ", n);
    scanf_s("%d", &id);

    printf("%d번 상품의 현재 재고수량: %d\n", id, arr[id - 1]);

    printf("전체 상품 재고 현황: ");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}
