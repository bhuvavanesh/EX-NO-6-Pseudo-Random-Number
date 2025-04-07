# EX-NO-6-Pseudo-Random-Number

## NAME:GOPIKRISHNAN M
## REG NO:212223043001


# AIM: 

Implementation of Pseudorandom Number Generation Using Standard library


# ALGORITHM:

1) Start the program and import the required libraries.
2) Seed the random number generator using the current time(i.e)
rand(time(0));
3) Get the number of randon number to generate.
4) Pass the value for number of iterations and print the numbers.
5) End the program.


# PROGRAM:
```
#include <stdio.h>
 #include <string.h>
 int main() {
 int i, j, k, l;
 char a[20], c[20], d[20];
 printf("\n\t\tRAIL FENCE TECHNIQUE\n");

 printf("\nEnter the input string: ");
 fgets(a, sizeof(a), stdin);

a[strcspn(a, "\n")] = '\0';
 l = strlen(a);
 for (i = 0, j = 0; i < l; i++) {
 if (i % 2 == 0) {
 c[j++] = a[i];
 }
 }
 for (i = 0; i < l; i++) {
 if (i % 2 == 1) {
 c[j++] = a[i];
 }
 }
 c[j] = '\0'; 
 printf("\nCipher text after applying rail fence: %s\n", c);
 // Rail fence decryption
 if (l % 2 == 0) {
 k =l / 2;
 } else {
 k =(l / 2) + 1;
 }
 for (i = 0, j = 0; i < k; i++) {
 d[j] = c[i];
 j += 2;
 }
 for (i = k, j = 1; i < l; i++) {
d[j] = c[i];
 j += 2;
 }
 d[l] = '\0'; 
 printf("\nText after decryption: %s\n", d);
 return 0; 
 }

```


# OUTPUT:

![image](https://github.com/user-attachments/assets/be93900f-f97d-4bc7-9e01-0119b0d3566d)



# RESULT:
The implementation of Pseudorandom Number Generation using Standard library is successful.
