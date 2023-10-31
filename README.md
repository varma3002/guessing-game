# guessing-game
Create a Guessing Game
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int secretNumber, guess, attempts = 0;
    srand(time(NULL)); // Seed the random number generator with the current time

    secretNumber = rand() % 100 + 1; // Generate a random number between 1 and 100

    printf("Welcome to the Guessing Game!\n");
    printf("I've selected a random number between 1 and 100. Try to guess it.\n");

    while (1) {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess < secretNumber) {
            printf("Too low! Try again.\n");
        } else if (guess > secretNumber) {
            printf("Too high! Try again.\n");
        } else {
            printf("Congratulations! You've guessed the number %d correctly in %d attempts.\n", secretNumber, attempts);
            break;
        }
    }

    return 0;
}
