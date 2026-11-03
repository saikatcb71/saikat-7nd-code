#include <stdio.h>

int main() {
    int n, i;
    float sum = 0.0, average;

    // Ask the user for the number of elements
    printf("Enter the number of elements (1 to 100): ");
    scanf("%d", &n);

    // Validate the input size
    if (n <= 0 || n > 100) {
        printf("Please enter a valid number between 1 and 100.\n");
        return 1;
    }

    float arr[n]; // Declare an array of size n

    // Read elements into the array
    printf("Enter %d numbers:\n", n);
    for (i = 0; i < n; i++) {
        printf("Element %d: ", i + 1);
        scanf("%f", &arr[i]);
        sum += arr[i]; // Add to sum as we take input
    }

    // Display the array elements
    printf("\nYou entered the following elements:\n");
    for (i = 0; i < n; i++) {
        printf("%.2f ", arr[i]);
    }

    // Calculate and display the results
    average = sum / n;
    printf("\n\nSum = %.2f\n", sum);
    printf("Average = %.2f\n", average);

    return 0;
}
