#include <stdio.h>
#include <string.h>

void bit_stuffing(char *input, char *output) {
    int count = 0;
    int j = 0;

    for (int i = 0; i < strlen(input); i++) {
        output[j++] = input[i];
        if (input[i] == '1') {
            count++;
            if (count == 5) {
                output[j++] = '0'; // Stuff a '0' after five consecutive '1's
                count = 0; // Reset count
            }
        } else {
            count = 0; // Reset count if '0' is encountered
        }
    }
    output[j] = '\0'; // Null-terminate the output string
}

int main() {
    char input[100], output[200];

    printf("Enter a binary string: ");
    scanf("%s", input);

    bit_stuffing(input, output);

    printf("Bit Stuffed Output: %s\n", output);
    return 0;
}
