# Mentober-CC-Tracking-Sheet
/* question link: https://leetcode.com/problems/increasing-decreasing-string/ */ 
class Solution {
    public String sortString(String s) {
        StringBuilder sb= new StringBuilder(); 
        int size= s.length();
        int frequency[]= new int[26]; 
      //  for (int i = 0; i < 26; i++)
         //   frequency[i]= 0; 
        for(int i=0;i<size;i++)
            frequency[s.charAt(i)-'a']++; 

        while(size>0)
        {
            for(int i=0;i<frequency.length;i++)
            {
                if(frequency[i]!=0)
                {
                    sb.append((char)(i+97)) ;
                        frequency[i]--;
                    size--;
                }
            }
            for(int i=frequency.length-1;i>=0;i--)
            {
                if(frequency[i]!=0)
                {
                    sb.append((char)(i+97)) ;
                        frequency[i]--;
                    size--;
                }
        }
        
    }
        return sb.toString();
}
}
