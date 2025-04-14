/***************************************************************************
Задача 1: Найти позицию буквы в алфавите
Напишите программу, которая определяет позицию заданной буквы в английском алфавите.
*******************************************************************************/

#include <stdio.h>
#include <string.h>

int main()
{
    char alfavit[] = {"abcdefghijklmnopqrstuvwxyz"};
    char letter = {'m'};
    int index = -1;
    
    int alfavit_size = sizeof(alfavit) / sizeof(alfavit[0]);
    for (int i = 0; i < alfavit_size; i++) {
        if (alfavit[i] == letter) {
            index = i;
            break;
        }
    }
    
    if (index != -1) {
        printf ("Буква(индекс) '%c' находится на позиции %d\n", letter, index);
    } else {
        printf ("Буква '%c' не найдена\n", letter);
    }
    
    return 0;
}
