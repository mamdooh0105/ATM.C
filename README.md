#include<stdio.h>

int main()
{
 int pin = 1234;
 int enteredPin;
 int choice;
 float balance;
 float amount;

 printf("==== WELCOME TO ATM ====\n");

 printf("Enter your PIN: ");
 scanf("%d", &enteredPin);

 if (enteredPin != pin)
 {
 printf("Invalid PIN!\n");
 return 0;
 }

 printf("\nLogin Successful!\n");

 do
 {
 printf("\n==== ATM MENU ====\n");
 printf("1. Check Balance\n");
 printf("2. Deposit Money\n");
 printf("3. Withdraw Money\n");
 printf("4. Exit\n");

 printf("Enter Your Choice: ");
 scanf("%d", &choice);

 switch (choice)
 {
  case 1:
  printf("Your Balance: Rs. %.2f\n", balance);
  break;

  case 2:
  printf("Enter Deposit Amount: ");
  scanf("%f", &amount);

  if (amount > 0)
  {
   balance = balance + amount;
   printf("Money Deposited Successfully!\n");
   printf("New balance: Rs. %.2f\n", balance);
  }
  else
  {
   printf("Invalid Amount!\n");
  }
  break;

  case 3:
   printf("Enter Withdrawl Amount: ");
   scan("%f", &amount);

   if (amount <= 0)
   {
    printf("Invalid Amount!\n");
   }
   else if (amount <= balance);
   {
    balance = balance - amount;
    printf("Please Collect Your Cash.\n");
   }
   else
   {
    printf("Insufficient Balance!\n");
   }
   break;

   case 4:
    printf("Thank You For Using ATM!\n");
    break;

   default:
    printf("Invalid Choice!\n");
  }
 }while (choice != 4);
 return 0;
}
