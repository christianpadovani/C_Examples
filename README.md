#include <stdio.h>

void hanoi(int n, char from, char to, char temp);


int main() 
{
    int n;
    
    printf("Quanti dischi utilizzare? ");
    scanf("%d", &n);
    printf("Eseguire le seguenti mosse:\n");
    hanoi(n, 'A', 'C', 'B');
    
    return 0;
}

void hanoi(int n, char from, char to, char temp) 
{
    if (n == 1) 
    {
        printf("Muovo il disco %d da %c a %c\n", n, from, to);
    }
    else 
    {
        hanoi(n - 1, from, temp, to);
        printf("Muovo il disco %d da %c a %c\n", n, from, to);
        hanoi(n - 1, temp, to, from);
    }
}
