# RAILWAY-TICKET-RESERVATION-SYSTEM
![Screenshot 2024-06-09 103501](https://github.com/akash6629/RAILWAY-TICKET-RESERVATION-SYSTEM/assets/99340063/d07948cd-55e4-4929-bb23-71d61f8c381b)


The provided C++ code implements a Railway Ticket Reservation System. The application allows users to view train information, book tickets, cancel tickets, and access administrative features such as adding or deleting trains and viewing passenger details. Here's a detailed explanation of the code:

### Libraries Used

- `#include <stdio.h>`: Standard input-output library for C functions.
- `#include <windows.h>`: Windows-specific functions.
- `#include <stdlib.h>`: Standard library for functions like `exit()`.
- `#include <conio.h>`: Console input-output functions.
- `#include <time.h>`: Functions for handling time.
- `#include <string.h>`: Functions for handling strings.

### Global Variables and Structures

- `struct adddata`: Stores train information such as serial number, train number, train name, start, destination, price, seat, and time.
- `struct bookticket`: Stores booking information such as train number, passenger name, phone number, date, and seat number.
- `add[]`: Array to store train details.
- `book[]`: Array to store booking details.
- `k`: Number of trains.
- `u`: Number of bookings.
- `trn_nmbr`, `name`, `phn`: Variables for temporary storage of train number, name, and phone number.

### Functions

- `main()`: Entry point of the program. Displays the main menu and handles user choices.
- `viewinfo()`: Displays train information.
- `bookticket()`: Handles ticket booking.
- `cancelticket()`: Handles ticket cancellation.
- `admin()`: Displays the admin menu and handles admin choices.
- `password()`: Authenticates admin using a predefined password.
- `dlttrain()`: Deletes a train from the system.
- `viewpassenger()`: Displays passenger details.
- `addtrain()`: Adds a new train to the system.
- `bookticket_write()`: Writes booking details to files.
- `viewpassengers_read()`: Reads booking details from files.
- `awrite()`: Writes train details to files.
- `aread()`: Reads train details from files.

### Main Menu

Displays the current date and time, and provides the following options:

1. View Information: Calls `viewinfo()`.
2. Book Ticket: Calls `bookticket()`.
3. Cancel Ticket: Calls `cancelticket()`.
4. Admin: Calls `password()` for admin authentication.
5. Exit: Exits the program.

### Admin Menu

Provides the following options:

1. View Passengers: Calls `viewpassenger()`.
2. Add Train: Calls `addtrain()`.
3. Delete Train: Calls `dlttrain()`.
4. Back: Returns to the main menu.

### Booking and Cancellation

- `bookticket()`: Prompts the user for train number and booking details. Checks availability and books tickets.
- `cancelticket()`: Prompts the user for phone number, finds the booking, and cancels the ticket.

### File Operations

- `bookticket_write()`: Writes booking information to `booklist.txt` and `booklistreport.txt`.
- `viewpassengers_read()`: Reads booking information from `booklist.txt` and `booklistreport.txt`.
- `awrite()`: Writes train information to `train_details.txt` and `train_report.txt`.
- `aread()`: Reads train information from `train_details.txt` and `train_report.txt`.

### Example Execution Flow

1. User starts the program.
2. Main menu is displayed.
3. User chooses an option (e.g., Book Ticket).
4. Corresponding function is called (e.g., `bookticket()`).
5. User inputs required details.
6. System processes the input and performs the required action.
7. Updated information is saved to files.
8. User is prompted to return to the main menu or exit.

### Improvements

- Use dynamic memory allocation instead of fixed-size arrays.
- Implement error handling for file operations.
- Use more secure methods for password handling.
- Enhance the user interface for better user experience.

This explanation covers the key components and flow of the Railway Ticket Reservation System. If you have any further questions or need additional details, feel free to ask!
