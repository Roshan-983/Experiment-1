# Experiment-1

#include <stdio.h>

int main() {
    int marks[5], i, total = 0;
    float average;

    printf("Enter marks for 5 subjects (out of 100):\n");

    for(i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%d", &marks[i]);

        // Simple validation
        if(marks[i] < 0 || marks[i] > 100) {
            printf("Invalid marks! Please enter between 0 and 100.\n");
            i--; // Ask again for the same subject
            continue;
        }

        total += marks[i];
    }

    average = total / 5.0;

    printf("\n--- Marks Summary ---\n");
    for(i = 0; i < 5; i++) {
        printf("Subject %d: %d\n", i + 1, marks[i]);
    }
    printf("Total Marks: %d\n", total);
    printf("Average Marks: %.2f\n", average);

    return 0;
}
