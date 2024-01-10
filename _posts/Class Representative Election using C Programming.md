
# Class Representative Election using C Programming

    -> Establishes a versatile and reliable voting system.
    -> Suitable for both large and small groups, such as a batch or a class.
    -> Maintains a comprehensive record of every voting process.

The is a simple Election Management System in C. The system is designed to handle the election process, allowing students to cast their votes and administrators to manage the election, view results, and perform administrative tasks.

# How to use?

## Once you have the files "MAIN.C" and "ELECTION.H", compile and run MAIN.C.
##### For Admin Panel, Use Username: "Admin" and Password: "admiN"

# Watch the Project Demo

## Video Demo: [Project Demo](https://clipchamp.com/watch/wZ85DD0J9iL)

**Components:**
1. **`election.h`**: Header file containing necessary declarations, structures, and function prototypes.

2. **`main.c`** (main program):
   - The program has an infinite loop representing the main menu.
   - Users can choose between the Student panel, Admin panel, or exit the system.
   - Depending on the user's choice, the corresponding panel (Student or Admin) is called.

**Admin Panel:**
- **New Election (Option 1):**
  - Initiates a new election, prompting the user to enter election details, candidate information, etc.
  - Creates candidate files and saves election information in files.
  
- **Continue Previous Election (Option 2):**
  - Loads election information from files, allowing administrators to continue the previous election.

- **Delete Illegal Vote (Option 3):**
  - Admin can delete votes based on user ID.

- **Ban User IDs (Option 4):**
  - Admin can ban specific user IDs, and the banned IDs are stored in a file.

- **Result (Option 5):**
  - Displays the election result, including the winner and each candidate's votes.
  - Provides voting percentage.

- **Logout (Option 6):**
  - Returns to the main menu.

**Student Panel:**
- **Voting Process:**
  - Students can enter their user ID and cast their votes for the available candidates.
  - The program checks the validity of the user ID, whether the user has already voted, and whether the user is banned.

- **Exit (Entering '0' as User ID):**
  - Allows students to exit the voting process.

**Authentication:**
- The Admin panel requires a simple username ('Admin') and password ('admiN') for authentication.

**Data Storage:**
- Election information, candidate details, and votes are stored in files.
- Banned user IDs are stored in the 'Banned.txt' file.

**Functions:**
- Functions for user authentication, banning IDs, creating candidate files, deleting illegal votes, and more.

**Global Variables:**
- Global variables include structures for current valid ID, an array for candidates, the number of candidates, and an array for student votes.

**Conclusion:**
This Election Management System provides a basic framework for handling elections in an educational institution. It allows students to cast their votes, administrators to manage the election process, and provides functionalities like banning IDs and viewing results.


