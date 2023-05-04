import java.util.Scanner;

public class LoginCredentials {

	public static void main(String[] args) {
		Scanner in = new Scanner(System.in);
		String userName;
		for (int i = 1; i<=3; i++) {
			System.out.print("User Name : ");
			userName = in.next();
			if (userName.equalsIgnoreCase("admin")){
				while(i++<=3) {
					String password;
					System.out.print("Password :");
					password = in.next();
					if (password.equals("admin123")) {
						System.out.println("Login Successful!");
						return;
					}
					else {
						System.out.println("Invalid password!");
					}
				}
			}
			else {
				System.out.println("Invalid username!");
			}
		}
		System.out.println("3 Attempts are over. Try after some time");
	}

}