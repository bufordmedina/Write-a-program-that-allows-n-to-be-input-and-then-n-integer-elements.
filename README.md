# Write-a-program-that-allows-n-to-be-input-and-then-n-integer-elements.
Write a program that allows n to be input, and then n integer elements.
import java.util.Scanner;
public class BaiTapJavaCoBan14
{
   public static void main(String[] args)
   {
      //Declare necessary variables
      int n;
      int[] soNguyen;
      Scanner sc = new Scanner(System.in);
      //Insert information
      System.out.println("Enter n:");
      n = sc.nextInt();
      soNguyen = new int[n];
      for (int i = 0; i < n; i++)
      {
         System.out.println("Enter Integer:");
         soNguyen[i] = sc.nextInt();
      }
      //Print the original array
      System.out.println("Array before reverse: ");
      for (int i = 0; i < n; i++)
         System.out.print(soNguyen[i] + " ");
      //Invert array
      for (int i = 0; i < n/2; i++)
      {
         int empty;
         empty = soNguyen[i];
         soNguyen[i] = soNguyen[n-i-1];
         soNguyen[n-i-1] = empty;
      }
      //Print the array after reversing
      System.out.println("\nArray after reversed: ");
      for (int i = 0; i < n; i++)
      System.out.print(soNguyen[i] + " ");
   }
}
