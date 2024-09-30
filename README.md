# st10233446.part-1
*/import java.util.Scanner;


public class St10233446Part1 {
    boolean checkUserName(){
        boolean underscore;
        underscore=userName.conatins("_");
        if (userName.length()<5 && underscore==true ) {
            System.out.println ("Username successfully captured");
            return true;
        }
    return false;
    }

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
       Scanner name1= new Scanner(System.in);
       System.out.println(" Enter username ");
       String userName;
       userName=name1.nextLine();
       checkUserName(userName);
    }
    
     public static void main(String[] args) {

    Scanner in = new Scanner(System.in);
    System.out.print("Please enter a given  password : ");
    String passwordhere = in.nextLine();
    System.out.print("Please re-enter the password to confirm : ");
    String confirmhere = in.nextLine();
    System.out.println("your password is: " + passwordhere);

    while (!passwordhere.equals(confirmhere) || !isValid(passwordhere)) {
        System.out.println("The password entered here  is invalid");
        System.out.print("Please enter the password again.it must be valid : ");
        String Passwordhere = in.nextLine();
        System.out.print("Please re-enter the password to confirm : ");

    }
}

public static boolean chechPasswordComplexity(String passwordhere) {

    if (passwordhere.length() < 8) {
        return false;
    } else {

        for (int p = 0; p < passwordhere.length(); p++) {
            if (Character.isUpperCase(passwordhere.charAt(p))) {
            }
        }
        for (int q = 0; q < passwordhere.length(); q++) {
            if (Character.isLowerCase(passwordhere.charAt(q))) {
            }
        }
        for (int r = 0; r < passwordhere.length(); r++) {
            if (Character.isDigit(passwordhere.charAt(r))) {
            }
        }
        for (int s = 0; s < passwordhere.length(); s++) {
            if (Character.isSpecialCharacter(passwordhere.charAt(s))) {
            } 
            }
            return true;
        }
    public class LoginUser {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice = 0;
        while (choice != 3) {
            System.out.println("Select an option: ");
            System.out.println("1. Register");
            System.out.println("2. Login");
            System.out.println("3. Quit");
            choice = scanner.nextInt();
            scanner.nextLine();
            switch (choice) {
                case 1:
                    registerUser(scanner);
                    break;
                case 2:
                    loginUser(scanner);
                    break;
                case 3:
                    break;
                default:
                    System.out.println("Invalid choice");
            }
        }
        scanner.close();
    }

    static void registerUser(Scanner scanner) {
        System.out.println("Enter your username:");
        String username = scanner.nextLine();
        System.out.println("Enter your password:");
        String password = scanner.nextLine();
        if (users.containsKey(username)) {
            System.out.println("User already exists.");
        } else {
            users.put(username, password);
            System.out.println("Registration successful.");
        }
    }

    static void loginUser(Scanner scanner) {
        System.out.println("Enter your username:");
        String username = scanner.nextLine();
        System.out.println("Enter your password:");
        String password = scanner.nextLine();
        if (!users.containsKey(username)) {
            System.out.println("Invalid username or password.");
        } else {
            if (users.get(username).equals(password)) {
                System.out.println("Login successful.");
            } else {
                System.out.println("Invalid username or password.");
            }
            
            String returnLoginStatus(String user,String password){
        if(loginUser(user, password)){
            return "Welcome "+firstName+lastName+" it is greater to see you again.";
        }
        else{
            return "Username or passoword incorrect, please try again.";
        }
        }
    }
}
