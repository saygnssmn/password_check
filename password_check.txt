package sifre_kontrol;

import java.util.Scanner;

public class password_check {
	public static void main(String[] args) {
	   boolean uzunlk_kntrl = false;
	   boolean bharf_kntrl = false;
	   boolean rakam_kntrl = false;  
	   Scanner input = new Scanner(System.in);
	   System.out.print("Sifreniz en az 8 karakterden olusmalidir\nSifrenizde en az bir buyuk harf ve en az bir rakam bulunmalidir..\nLutfen sifrenizi giriniz: "); 
	   String sifre = input.next();	  
	   for(int i=0;i<sifre.length();i++)
	     {
	         char s=sifre.charAt(i);          
	       if(Character.isUpperCase(s)) 
	           {
	    	   bharf_kntrl = true;
	           }	     
	       if(Character.isDigit(s)) // This verifies there is a digit
	           {
	    	   rakam_kntrl = true;
	           }       
	       if (sifre.length() >= 8) // This verifies the password is atleast 6 characters
	       {
	    	   uzunlk_kntrl= true;
	       }	       
	     }
	   if(bharf_kntrl == true && rakam_kntrl == true && uzunlk_kntrl == true)
       {
		   System.out.print( "Sifreniz olusturuldu!");
       }
	   if(bharf_kntrl == false )
	           {
		   System.out.print("\nSifrenizde en az bir buyuk harf olmali! \n");
	           }
	   if(rakam_kntrl == false)
	       {
		   System.out.print( "Sifrenizde en az bir rakam olmali!\n");
	       }
	   if(uzunlk_kntrl == false)
       {
		   System.out.print("Sifrenizde en az 8 karakterden olusmali!\n");
       }	 
	   }
	   }

	   
