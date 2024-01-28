#include <cs50.h>
#include <stdio.h>

int main(void)
{
    //Допуск цілих чисел лише від 1 до 8
    int h;
    do
    {
        h = get_int("Height: ");
    }
    while (h < 1 || h > 8);

    //Побудова піраміди з пропуском у 2 пробіла по центру
    int a = h - 1;
    int n = 1;
    for(int i = 0; i < h; i++)
    {
        for(int j = 0; j < a; j++)
        {
            printf(" ");
        }
        for(int k = 0; k < n; k++)
        {
            printf("#");
        }
        printf("  ");//Як умістити центр в цикл зі змінною "n" або позбавитися від копіювання, яке я зробив із циклом?
        for(int k = 0; k < n; k++)
        {
            printf("#");
        }
        a--;
        n++;
        printf("\n");
    }
}
