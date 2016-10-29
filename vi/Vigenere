#include <cs50.h>
#include <stdio.h>
#include <ctype.h>
#include <string.h>


int main(int argc, string argv[]) {
    if (argc != 2) {
        printf("Please, try again.");
        return 1;
    }

    string code = argv[1];
    unsigned long keyCount = strlen(code);
    //Перевіряємо чи ключ включає лише літери.
    for(int j = 0; j < keyCount; j++) {
        if (!isalpha(code[j])) {
            printf("Please, try again.");
            return 1;
        }
    }

    string userInput = GetString();
    //Шифрумуэмо текст в змінну userInput.
    //n++%keyCount - чергує літери в code і починає з початку,коли закінчуються.
    //65 перший номер великої букви в таблиці ASCII,а 97 перший номер малої букви.Ми їх додаємо і віднімаємо,щоб вони не виходили за межі літер.
    for (int i = 0, n = 0; i < strlen(userInput); i++) {
        if (isalpha(userInput[i])) {
            if (isupper(userInput[i]))
                printf("%c", ((((userInput[i] - 65) + ((toupper(code[n++%keyCount]))-65)%26) % 26) + 65));

            if (islower(userInput[i]))
                printf("%c", ((((userInput[i] - 97) + ((tolower(code[n++%keyCount]))-97)%26) % 26) + 97));
        } else
            printf("%c", userInput[i]);
    }

    printf("\n");
    return 0;
