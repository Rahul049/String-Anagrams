# String-Anagrams
import java.util.Scanner;

public class Solution {

    static boolean isAnagram(String a, String b) {
        String x= a.toLowerCase();
        String y=b.toLowerCase();
        if(x.length()!=y.length())
        {
            return false;
        }
        else
        {
            char A[]= x.toCharArray();
            StringBuilder B= new StringBuilder(y);
            for(int i=0;i<x.length();i++){
                String z=Character.toString(A[i]);
                {int j=B.indexOf(z);
                if(j==-1){ return false;}
                else     {B.deleteCharAt(j);}
              
                }
                              
            }
            if(B.length()==0){
                return true;
            }
            else
            {
                return false;
            }
        }
       
    }

    public static void main(String[] args) {
    
        Scanner scan = new Scanner(System.in);
        String a = scan.next();
        String b = scan.next();
        scan.close();
        boolean ret = isAnagram(a, b);
        System.out.println( (ret) ? "Anagrams" : "Not Anagrams" );
    }
}
