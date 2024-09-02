#include <iostream>
#include <vector>

// Function to print the divisors in decreasing order
void printDivisors(int number) {
    std::vector<int> divisors;

    // Find all divisors of the number
    for (int i = 1; i <= number; ++i) {
        if (number % i == 0) {
            divisors.push_back(i);
        }
    }

    // Print the divisors in decreasing order
    for (auto it = divisors.rbegin(); it != divisors.rend(); ++it) {
        std::cout << *it << std::endl;
    }
}

int main() {
    int number;
    char response;

    std::cout << "This program is designed to exhibit the positive divisors of positive integers supplied by you."
              << std::endl
              << "The program will repeatedly prompt you to enter a positive integer."
              << std::endl
              << "Each time you enter a positive integer, the program will print all the divisors of your integer in a column and in decreasing order."
              << std::endl
              << "You can terminate the program by entering 'N' (or 'n') when asked if you want to continue."
              << std::endl;

    do {
        // Prompt the user for a positive integer
        std::cout << "Please enter a positive integer: ";
        std::cin >> number;

        if (number <= 0) {
            std::cout << number << " is not a positive integer." << std::endl;
            // Skip the rest of the loop and prompt again
            continue;
        }

        // Print the divisors of the number
        printDivisors(number);

        // Ask if the user wants to enter another integer
        std::cout << "Would you like to see the divisors of another integer (Y/N)? ";
        std::cin >> response;

        while (response != 'Y' && response != 'y' && response != 'N' && response != 'n') {
            std::cout << "Please respond with Y (or y) for yes and N (or n) for no." << std::endl;
            std::cout << "Would you like to see the divisors of another integer (Y/N)? ";
            std::cin >> response;
        }

    } while (response == 'Y' || response == 'y');

    return 0;
}
