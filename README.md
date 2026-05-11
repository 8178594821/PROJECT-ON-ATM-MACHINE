💰 Mini Bank Management System (Java)

📌 Overview
This is a simple console-based Bank Management System built using Java.  
It allows users to perform basic banking operations like checking balance, withdrawing money, and depositing money.

🚀 Features
- ✅ Check Account Balance
- 💸 Withdraw Money
- 💰 Deposit Money
- ❌ Exit System

  🧠 How It Works
1. User selects an option from the menu
2. Program performs the selected operation
3. Menu continues until user exits

code:

import java.util.Scanner;

class BankApp {

    float balance = 1000; // Initial Balance
    Scanner sc = new Scanner(System.in);

    public void menu() {
        while (true) {
            System.out.println("\n===== BANK MENU =====");
            System.out.println("1. Check Account Balance");
            System.out.println("2. Withdraw Money");
            System.out.println("3. Deposit Money");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");

            int opt = sc.nextInt();

            switch (opt) {
                case 1:
                    checkBalance();
                    break;

                case 2:
                    withdrawMoney();
                    break;

                case 3:
                    depositMoney();
                    break;

                case 4:
                    System.out.println("Thank you for using our bank 😊");
                    return;

                default:
                    System.out.println("Invalid choice! Try again.");
            }
        }
    }

    public void checkBalance() {
        System.out.println("Current Balance: ₹" + balance);
    }

    public void withdrawMoney() {
        System.out.print("Enter amount to withdraw: ");
        float amount = sc.nextFloat();

        if (amount > balance) {
            System.out.println("❌ Insufficient Balance");
        } else {
            balance -= amount;
            System.out.println("✅ Withdrawal Successful");
        }
    }

    public void depositMoney() {
        System.out.print("Enter amount to deposit: ");
        float amount = sc.nextFloat();

        balance += amount;
        System.out.println("✅ Deposit Successful");
    }

    public static void main(String[] args) {
        BankApp obj = new BankApp();
        obj.menu();
    }
}

▶️ Sample Output

BANK MENU

Check Account Balance
Withdraw Money
Deposit Money
Exit
Enter your choice: 1
Current Balance: ₹1000

⭐ If you like this project
Give it a ⭐ on GitHub and follow for more projects 🚀
