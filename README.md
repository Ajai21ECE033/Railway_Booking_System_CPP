# Railway Reservation System

## Overview

The Railway Reservation System is a C++ console application that simulates the process of booking, cancelling, and managing train tickets. This project demonstrates the use of object-oriented programming principles, including classes, inheritance, and data structures like vectors, maps, and queues.

## Features

- **Book Tickets:** Passengers can book tickets specifying their berth preferences (lower, middle, upper).
- **Cancel Tickets:** Allows passengers to cancel their booked tickets.
- **View Booked Tickets:** Displays all booked tickets along with passenger details.
- **View Available Tickets:** Shows the number of available lower, middle, upper berths, RAC, and waiting list positions.

## Classes

1. **Passenger:** Contains details about each passenger, such as name, age, gender, berth preference, and seat allocation.
2. **Ticket:** Handles the booking and cancellation of tickets, and manages the available berths, RAC, and waiting list positions.
3. **Main:** The driver class that interacts with the user and facilitates the functioning of the railway reservation system.

## Data Structures

- **Vectors:** Used for storing seat positions for lower, middle, upper berths, RAC, and waiting list.
- **Map:** Used for storing confirmed tickets with passenger IDs as keys.
- **Queues:** Used for managing RAC and waiting list passengers.

## How to Run

1. **Compile the Program:**
    ```sh
    g++ railway_reservation.cpp -o railway_reservation
    ```

2. **Run the Executable:**
    ```sh
    ./railway_reservation
    ```

## Usage

Upon running the program, a menu will be displayed with the following options:

1. **Book Ticket:** Enter passenger details and berth preference to book a ticket.
2. **Cancel Ticket:** Enter the passenger ID to cancel the ticket.
3. **View Booked Tickets:** Display the list of all booked tickets.
4. **View Available Tickets:** Show the current status of available tickets.
5. **Exit:** Exit the program.

## UML Diagram

The UML diagram provides a high-level overview of the classes and their relationships within the Railway Reservation System.

```plaintext
+-----------------+        +-----------------+        +-----------------+
|   Passenger     |        |     Ticket      |        |      Main       |
+-----------------+        +-----------------+        +-----------------+
| - name: string  |        | - lowerBerths:  |        | - ticket: Ticket|
| - age: int      |        | - int           |        +-----------------+
| - gender: char  |        | - upperBerths:  |        | + run()         |
| - berthPref:    |        | - int           |        | + bookTicket()  |
|   string        |        | - middleBerths: |        | + cancelTicket()|
| - passId: int   |        | - int           |        | + viewBookedTix()|
| - alloted:      |        | - rac: int      |        | + viewAvailTix()|
|   string        |        | - waitingList:  |        +-----------------+
| - seatNum: int  |        | - int           |
+-----------------+        | - lowerPos:     |
                           |   vector<int>   |
                           | - middlePos:    |
                           |   vector<int>   |
                           | - upperPos:     |
                           |   vector<int>   |
                           | - racPos:       |
                           |   vector<int>   |
                           | - waitPos:      |
                           |   vector<int>   |
                           | - confirmedTix: |
                           |   map<int,      |
                           |   Passenger>    |
                           | - racPassengers:|
                           |   queue<int>    |
                           | - waitPassengers:|
                           |   queue<int>    |
                           +-----------------+
```

## Contribution

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

---

By providing this detailed README, you will help others understand your project and use it effectively.
