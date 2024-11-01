# COP2334-1-Midterm-Lab-Activity-Question-1
This is a GitHub repository link for the answer to question 1 of the midterm lab activities

// This program is used to calculate the toll fee based on the time of day and type of day.

// Include the header file.
#include <iostream> // For input and output
using namespace std; // For cin, cout, endl

// Declare the namespace
double CalcToll(int hour, bool isMorning, bool isWeekend) {
  if (isWeekend) { // If it is a weekend
    if (hour < 7) { // If it is before 7:00 AM
      return 6.05; // Return the toll fee
    }
    else if (hour >= 7 && hour < 20) { // If it is between 7:00 AM and 8:00 PM.
      return 7.15; // Return the toll fee
    }
    else { // If it is after 8:00 PM
      return 6.10; // Return the toll fee
    }
  }
  else { // If it is not a weekend
    if (hour < 7) { // If it is before 7:00 AM
      return 6.15; // Return the toll fee
    }
    else if (hour >= 7 && hour < 10) { // If it is between 7:00 AM and 10:00 AM.
      return 7.95; // Return the toll fee
    }
    else if (hour >= 10 && hour < 15) { // If it is between 10:00 AM and 3:00 PM.
      return 6.90; // Return the toll fee
    }
    else if (hour >= 15 && hour < 20) { // If it is between 3:00 PM and 8:00 PM.
      return 8.95; // Return the toll fee
    }
    else { // If it is after 8:00 PM
      return 6.40; // Return the toll fee
    }
  }
}

// Main function
int main() { // Start of the main function
  int time; // Declare the variable
  bool isMorning; // Declare the variable
  bool isWeekend; // Declare the variable
  cout << "Enter the time of day: "; // Prompt the user to enter the time of day.
  cin >> time; // Get the time of day from the user.
  cout << "Enter if it's morning (1) or the afternoon (0): "; // Prompt the user to enter if it's morning or the afternoon.
  cin >> isMorning; // Get if it's morning or the afternoon from the user.
  cout << "Enter if it's a weekday (1) or weekend (0): "; // Prompt the user to enter if it's a weekday or weekend.
  cin >> isWeekend; // Get if it's a weekday or weekend from the user.
  cout << "The toll fee is: $" << CalcToll(time, isMorning, isWeekend) << endl; // Display the toll fee.
  return 0; // Return 0 and exit the program.
}
