# Banking System Assignment

This README file provides an overview and explanation of the `banking_system_assignment.cpp` program, which implements a simple banking system using object-oriented programming in C++. The program allows users to manage accounts, perform transactions, and view account details through a menu-driven interface.

## Features

The banking system supports the following operations:

1. **Create an Account:** Create a new account with a unique account number, client name, address, and initial deposit.
2. **Deposit Money:** Add money to an existing account.
3. **Withdraw Money:** Withdraw money from an account, with validation for sufficient balance.
4. **Check Balance:** Display the current balance of an account.
5. **Close an Account:** Permanently remove an account from the system.
6. **Display Account Information:** View details such as the account holder's name, address, and current balance.
7. **Transaction History:** View the history of all transactions performed on an account.
8. **Exit Program:** Exit the application.

## Code Structure

### Classes

#### `Account`
Represents an individual bank account.

- **Attributes:**
  - `name`: Name of the account holder.
  - `address`: Address of the account holder.
  - `account_number`: Unique account identifier.
  - `balance`: Current balance in the account.
  - `transaction_history`: Records of all transactions performed on the account.

- **Methods:**
  - Constructor: Initializes account with name, address, account number, and initial deposit.
  - `deposit(int amount)`: Adds the specified amount to the balance and logs the transaction.
  - `withdraw(int amount)`: Deducts the specified amount if sufficient balance exists; logs the transaction.
  - `display_transaction_history() const`: Displays all transactions performed on the account.
  - `display_account_info() const`: Displays account holder's information.
  - Getters for `balance` and `account_number`.

#### `Bank`
Manages multiple accounts and provides a higher-level interface for banking operations.

- **Attributes:**
  - `accounts`: Vector of `Account` objects representing all accounts in the bank.
  - `next_account_number`: Auto-increments to assign unique account numbers.

- **Methods:**
  - `create_account(string name, string address, int initial_deposit)`: Creates and adds a new account.
  - `deposit(int account_number, int amount)`: Deposits money into a specified account.
  - `withdraw(int account_number, int amount)`: Withdraws money from a specified account.
  - `check_balance(int account_number)`: Displays the balance of a specified account.
  - `close_account(int account_number)`: Removes an account by its number.
  - `display_account_info(int account_number)`: Displays details of a specified account.
  - `display_transaction_history(int account_number)`: Shows transaction history for a specific account.

### Main Program

The `main` function provides a menu-driven interface that allows users to interact with the banking system:

1. **Display Menu:** Shows the available options.
2. **Process Input:** Executes the selected operation based on user input.
3. **Loop:** Repeats until the user chooses to exit.

## How to Run the Program

1. Compile the program using a C++ compiler:
   ```
   g++ banking_system_assignment.cpp -o banking_system
   ```

2. Run the compiled executable:
   ```
   ./banking_system
   ```

3. Follow the on-screen prompts to navigate the menu and perform banking operations.

## Example Usage

- **Creating an Account:**
  - Input the name, address, and initial deposit.
  - The program will generate a unique account number and confirm account creation.

- **Depositing Money:**
  - Enter the account number and deposit amount.
  - The program updates the balance and confirms the transaction.

- **Transaction History:**
  - View a log of all past transactions for a specific account.

## Limitations

- The program does not persist data between runs. All account information is stored in memory and will be lost upon exiting.
- Input validation is minimal. Users must provide valid inputs to avoid undefined behavior.

## Future Improvements

- Add file-based or database storage for account persistence.
- Implement additional security measures such as account authentication.
- Provide more robust error handling and input validation.
- Add interest calculation for savings accounts or support for different account types.

## License

This project is open-source and free to use for educational purposes.

