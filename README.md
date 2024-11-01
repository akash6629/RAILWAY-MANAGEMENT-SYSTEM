# RAILWAY MANAGEMENT SYSTEM
![Screenshot 2024-06-09 103501](https://github.com/akash6629/RAILWAY-TICKET-RESERVATION-SYSTEM/assets/99340063/d07948cd-55e4-4929-bb23-71d61f8c381b)


Certainly! Here’s an explanation of the Railway Management System C++ code provided, structured similarly to your example:

---

## Railway Management System

The Railway Management System is a C++ program that allows users to manage train information, book and cancel tickets, and provides an admin interface to add or delete trains and view passenger details.

### Libraries Used

- `#include <iostream>`: For basic input-output operations.
- `#include <fstream>`: For reading from and writing to files.
- `#include <string>`: For using the `string` data type.
- `#include <vector>`: For using dynamic arrays with the `vector` data type.
- `#include <ctime>`: For handling date and time.

### Classes

1. **`Train`**:
   - Holds information about each train, such as:
     - `serial_number`: A unique identifier for each train.
     - `train_number`: The official number of the train.
     - `train_name`: The name of the train.
     - `start` and `destination`: Start and end locations of the train.
     - `price`: The price of the ticket.
     - `seats`: Number of available seats.
     - `time`: Scheduled departure time.

2. **`Booking`**:
   - Stores booking information for each passenger:
     - `train_number`: The train being booked.
     - `passenger_name`: Name of the passenger.
     - `phone_number`: Contact number for the passenger.
     - `date`: Date of travel.
     - `seat`: The assigned seat number.

3. **`RailwayManagementSystem`**:
   - This is the main class managing all operations. It contains:
     - **Data Members**:
       - `trains`: A list of all train records.
       - `bookings`: A list of all bookings.
     - **Private Methods**:
       - `loadTrainData()`: Loads train data from `train_details.txt`.
       - `loadBookingData()`: Loads booking data from `booklist.txt`.
       - `saveTrainData()`: Saves the current train data to `train_details.txt`.
       - `saveBookingData()`: Saves the current booking data to `booklist.txt`.
     - **Public Methods**:
       - `viewInfo()`: Displays all available trains with details.
       - `bookTicket()`: Allows a user to book a ticket by selecting a train and entering their details.
       - `cancelTicket()`: Allows a user to cancel their ticket based on their phone number.
       - `admin()`: Provides an admin menu to view all bookings, add a train, and delete a train.

### Program Flow

1. **Main Menu**:
   - Displayed in the `main()` function. Shows options to view information, book or cancel a ticket, access admin functions, or exit.
   - Calls corresponding functions in the `RailwayManagementSystem` class based on user selection.

2. **Functions and Their Roles**:
   
   - **`viewInfo()`**:
     - Displays a list of all available trains with details such as the train number, name, start and destination points, price, seats, and time.

   - **`bookTicket()`**:
     - Prompts the user to enter the number of tickets, train number, date, passenger name, and phone number.
     - Checks seat availability, assigns a seat, reduces available seats, and saves the booking.

   - **`cancelTicket()`**:
     - Asks the user for their phone number, searches for their booking, restores the seat, and deletes the booking.
   
   - **`admin()`**:
     - Displays the admin menu with options:
       - **View Passengers**: Shows a list of passengers with their booking details.
       - **Add Train**: Adds a new train to the system, prompting the admin for details.
       - **Delete Train**: Deletes a train from the system based on its train number.
     
3. **File Operations**:
   - The program uses `train_details.txt` to store train data and `booklist.txt` to store booking data.
   - **Data Loading**: On startup, train and booking data are loaded into vectors.
   - **Data Saving**: After each operation (booking, cancellation, adding/deleting trains), updated data is saved back to the files.

### Example Execution Flow

1. The user runs the program.
2. The main menu is displayed.
3. The user chooses an option (e.g., book a ticket).
4. Corresponding function (`bookTicket`) is executed.
5. User enters required information (train number, date, name, etc.).
6. System checks availability and assigns a seat if available.
7. Booking details are saved, and the user is redirected to the main menu or can choose to exit.

### Potential Improvements

1. **Dynamic Memory Allocation**: Use pointers for improved memory efficiency, especially with larger datasets.
2. **File Handling Error Checking**: Add error checking for file operations to handle cases where files might be missing or unreadable.
3. **Enhanced UI**: Use a more user-friendly console interface.
4. **Improved Security**: Use hashed passwords for admin authentication.

### Example Output

```plaintext
=================================
=   RAILWAY MANAGEMENT SYSTEM   =
=================================

[1] VIEW INFORMATION
[2] BOOK TICKET
[3] CANCEL TICKET
[4] ADMIN
[5] EXIT

ENTER YOUR CHOICE: 
```

This explanation covers the main components and flow of the Railway Management System program. If you have further questions or need additional details, feel free to ask!
