# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>

int main()
{
    char s[100], e[100];
    int i, key;

    printf("Enter text: ");
    scanf(" %[^\n]", s);

    printf("Enter key: ");
    scanf("%d", &key);
    key = key % 26;

    for(i = 0; s[i] != '\0'; i++)
    {
        if(s[i] >= 'a' && s[i] <= 'z')
            e[i] = (s[i] - 'a' + key) % 26 + 'a';
        else if(s[i] >= 'A' && s[i] <= 'Z')
            e[i] = (s[i] - 'A' + key) % 26 + 'A';
        else
            e[i] = s[i];
    }
    e[i] = '\0';

    printf("Encrypted: %s\n", e);

    for(i = 0; e[i] != '\0'; i++)
    {
        if(e[i] >= 'a' && e[i] <= 'z')
            e[i] = (e[i] - 'a' - key + 26) % 26 + 'a';
        else if(e[i] >= 'A' && e[i] <= 'Z')
            e[i] = (e[i] - 'A' - key + 26) % 26 + 'A';
    }

    printf("Decrypted: %s\n", e);

    return 0;
}
```

## OUTPUT:
<img width="1918" height="1028" alt="Screenshot 2026-10-22 091757" src="https://github.com/user-attachments/assets/faeaf490-ab87-4b98-aa0e-7605f9437196" />


## RESULT :
Thus the implementation of ceasar cipher had been executed successfully.
