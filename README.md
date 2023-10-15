package Package1;
import java.util.Scanner;

public class characterString 
{
static String CharactersString(String input) 
{
   char[] chars = input.toCharArray(); 
   for (int i = 0; i < chars.length; i++) 
   {
	  char c = chars[i];
	  if (Character.isUpperCase(c)) 
	  {
		 chars[i] = (char) (((c - 'A' - 2 + 26) % 26) + 'A');  //upper case letters by 2 characters
	  } 
   else if (Character.isLowerCase(c)) 
   {
	   chars[i] = (char) (((c - 'a' - 3 + 26) % 26) + 'a');  //lower case letters by 3 characters
	   }
   }
    return new String(chars);
}

public static void main(String[] args)
{
     Scanner sc = new Scanner(System.in);
	 System.out.print("Enter a string: ");
	 String input = sc.nextLine();
	 String characters = CharactersString(input);
	 System.out.println("Shifted string: " + characters);
}
}


O/P;

Enter a string: "Hello"
Shifted string: "Fbiil"
