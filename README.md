# solid-octo-garbanzo
def main():
    # Initialize account details
    account_number = 1234567
    pin = 1234
    balance = 10000

    # Validate account number
    for i in range(3):
        entry_account = int(input("Please enter your bank account number: "))
        if entry_account == account_number:
            break
        else:
            print(f"Wrong account number! You have {3 - i} attempts left...")
    else:
        print("Account blocked")
        exit(0)

    # Validate PIN
    for k in range(3):
        entry_pin = int(input("Please enter your PIN: "))
        if entry_pin == pin:
            break
        else:
            print(f"Wrong PIN! You have {3 - k} attempts left!!")
    else:
        print("PIN blocked")
        exit(0)

    # Perform transaction
    if entry_pin == pin and entry_account == account_number:
        transaction_choice = int(input("Please enter the type of transaction:\n1. Check balance\n2. Deposit\n3. Withdraw cash\n"))
        if transaction_choice == 1:
            print(f"Your balance is {balance}")
        elif transaction_choice == 2:
            customer_deposit = float(input("Please enter the amount you want to deposit: "))
            balance += customer_deposit
            print(f"You successfully deposited {customer_deposit} into your account.")
            print(f"Your new balance is {balance}")
        else:
            print("Invalid transaction choice. Exiting...")

if __name__ == "__main__":
    main()
