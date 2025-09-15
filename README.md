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
#include <ctype.h>

void caesarCipher(char* text, int shift) {
    for (int i = 0; text[i] != '\0'; i++) {
        char ch = text[i];
        
 
        if (isupper(ch)) {
            ch = (ch + shift - 'A') % 26 + 'A';
        }
        
        else if (islower(ch)) {
            ch = (ch + shift - 'a') % 26 + 'a';
        }

        text[i] = ch;
    }
}

int main() {
    char text[100];
    int shift;

   
    printf("Enter a plaintext: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter shift value: ");
    scanf("%d", &shift);

  
    caesarCipher(text, shift);

  
    printf("Ciphertext: %s\n", text);

    return 0;
}
```

## OUTPUT:
<img width="451" height="210" alt="image" src="https://github.com/user-attachments/assets/f2ed6c89-61d5-425a-84a9-9ed1139d135d" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
