import java.util.*; 
public class bankdetails
{

	public static void main(String[] args) 
	{
		int balance=5000, withdraw, deposite, num;
		Scanner sc = new Scanner (System.in);
		while(true)
		{
			System.out.println("Welcome to my ATM machine");
			System.out.println("1. Withraw");
			System.out.println("2. Deposite");
			System.out.println("3. Check Balance");
			System.out.println("4. Exit");
			num = sc.nextInt();
			
			switch(num)
			{
			case 1:
				System.out.println("Enter amount to be withdraw");
				withdraw = sc.nextInt();
				if(balance>=withdraw)
				{
					balance = balance-withdraw;
					System.out.println("balance amount is:"+balance);
					System.out.println("Please collect your money");
				}
				
				else
				{
					System.out.println("You don't have enough money for withdraw");
				}
					System.out.println(" ");
					
					break;
					
			case 2:
				System.out.println("Enter amount to be Deposite");
				deposite = sc.nextInt();
				balance = balance+deposite;
				System.out.println("Your balance amount is: " +balance);
				System.out.println("money has been deposite successfully");
				System.out.println(" ");
				break;
				
			case 3:
				System.out.println("Balance of your account is: "+balance);
				System.out.println(" ");
				break;
				
			case 4:
				System.exit(0);
				System.out.println("Thank you for using ATM, BYE...  BYE.... ");
			
			}
		}
	}

}
