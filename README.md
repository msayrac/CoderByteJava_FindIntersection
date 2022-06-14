# CoderByteJava_FindIntersection
import java.util.*; 
import java.io.*;

class Main {

  public static String FindIntersection(String[] strArr) {
    // code goes here

    String str0 = strArr[0];

    str0 = str0.replaceAll(", ", ",");
    

   String[] str00=str0.split(",");

    
String str1 = strArr[1];
    str1 = str1.replaceAll(", ", ",");
   String[] str11=str1.split(",");

String add ="";

for(int i=0; i<str00.length; i++){

  for(int j=0; j<str11.length; j++){  
   if(str00[i].equals(str11[j])){
      add +=" "+str00[i];
    }  
  }  
}
add=add.trim();
add=add.replace(" ",",");
if(add==""){
  System.out.println("false");
} else{
  System.out.println(add);
}
    return "";
  }

  public static void main (String[] args) {  
    // keep this function call here     
    Scanner s = new Scanner(System.in);
    System.out.print(FindIntersection(s.nextLine())); 
  }

}
