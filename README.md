# Mentober-CC-Tracking-Sheet
/* question link: https://www.codechef.com/problems/CHEFEZQ */ 
import java.util.*;
import java.lang.*;
import java.io.*;
class Codechef
{
 public static void main (String[] args) throws java.lang.Exception
 {
  Scanner sc = new Scanner(System.in);
  long t = sc.nextLong();
  
  while(t > 0){
      int n = sc.nextInt();
      long k = sc.nextLong();
      long arr[] = new long[n];
         long sum =0,day=0,flag=0;
          for(int i=0;i<n;i++){
              arr[i] = sc.nextLong();
              sum += arr[i];
          }
      
      for(int i=0;i<n-1;i++){
          if(arr[i] < k){
              flag =1;
              day =i;
              break;
          }
          arr[i+1] += (arr[i]-k);
       }
       
        
           if(flag == 1){
               System.out.println(day+1);
           }
           else{
                     day = (sum / k)+1;
               System.out.println(day);
           }
       
           t--;
  }
 }
}
