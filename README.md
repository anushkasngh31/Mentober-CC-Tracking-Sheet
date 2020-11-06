# Mentober-CC-Tracking-Sheet
/* question link: https://leetcode.com/problems/reverse-words-in-a-string/ */
class Solution {
    public String reverseWords(String s) {
         if(s.length()==0) return s; 
        
        int n= s.length();
        int begin=0; 
        String result= ""; 
        
        while(begin<n)
        {   
            String word=""; 
            while(begin<n && s.charAt(begin)==' ')
                begin++; 
            if(begin>=n) break; 
            int end= begin+1; 
            while(end<n && s.charAt(end)!=' ')
                end++; 
        
            word= s.substring(begin,end); 
            if(result.length()==0) result= word; 
            else
            result= word + " " + result; 
            begin= end+1; 
        }
        return result; 
    }
}
