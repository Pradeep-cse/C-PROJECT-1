#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    std::srand(std::time(0));
    
    int randomNumber = std::rand() % 100 + 1;
    int userGuess = 0;
    
    std::cout << "Welcome to the Number Guessing Game!" << std::endl;
    std::cout << "You have to select a number between 1 and 100." << std::endl;

    while (true) {
        std::cout << "Enter your guess: ";
        std::cin >> userGuess;

        if (userGuess > randomNumber) {
            std::cout << "Too high! Try again." << std::endl;
        } else if (userGuess < randomNumber) {
            std::cout << "Too low! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed the correct number!" << std::endl;
            break;
        }
    }

    return 0;
}
