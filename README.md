//# TopFive
//Computer Concepts


import java.io.BufferedWriter;
import java.io.BufferedReader;
import java.io.File;
import java.io.FileWriter;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;
import java.util.ArrayList;

public class TopFive {

static String sCurrentLine;
static ArrayList<String> fileArray = new ArrayList<String>();
static ArrayList<String> rankArray = new ArrayList<String>();
static ArrayList<String> commentArray = new ArrayList<String>();
static String inputFile = "C:/Users/EJL114/Desktop/input.txt";
static String outputFile= "C:/Users/EJL114/Desktop/output.txt";
static String answer;
static int rank;
static boolean inputError = false;
static Scanner myScanner = new Scanner(System.in);
	
public static void main(String[] args) {
do{
	promptUser();
             readFile();
        }            while (inputError == true);
                      for (int i = 0; i < fileArray.size(); i++){
                      System.out.println(fileArray.get(i));
               }
	                rank();
       }

public static void promptUser(){
   System.out.println("Please enter file directory: ");
	inputFile = myScanner.nextLine();
	 }
　
public static void readFile(){

try {
	
        BufferedReader reader = new BufferedReader(new.             FileReader(inputFile));
         while ((sCurrentLine = reader.readLine()) != null) {
          fileArray.add(sCurrentLine);
          inputError = false;
          }
} catch (IOException e) { //system reports if file isn't valid
         System.out.println("File not found. Please enter.  new file name.");
          inputError = true;
          }
}
, but 

	public static void rank(){
		
		for (int i = 0; i < fileArray.size(); i++){
		         System.out.println(fileArray.get(i)); //print out item
		
		         try{
		                System.out.println("Rank: ");
		                answer = myScanner.nextLine();
		                rank = Integer.parseInt(answer.trim()); //is the input an integer?
		                
		                if (rank < 0 || rank > fileArray.size()) { //make sure its a valid rank
		                	System.out.println("I'm sorry -" + rank + " is not good");
		                	inputError = true;
		                }
		                else {
		   					 inputError = false;
		   				 }
	           } catch (Exception e) { //inputs not an integer
	        	   	System.out.println("I'm sorry -" + rank + " is not an integer!!");
	   				inputError = true;
	           }
		
			}
		}


}


