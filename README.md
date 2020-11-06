# Mentober-CC-Tracking-Sheet
/* question link: https://leetcode.com/problems/reformat-date/description/ */ 
class Solution {
    public String reformatDate(String date) {
        String output=""; String month="";
         
        if(date.length()==12)
        {
            output+= date.substring(8);
            month+= date.substring(4,7);
        }
        else if(date.length()== 13)
        {
            output+= date.substring(9); 
            month= date.substring(5,8); 
        }
        output+= "-"; 
        switch(month)
        {
                case "Jan": output+= "01"; 
                        break;
                case "Feb": output+= "02"; 
                        break;
                case "Mar": output+= "03"; 
                        break;
                case "Apr": output+= "04"; 
                        break;
                case "May": output+= "05"; 
                        break;
                case "Jun": output+= "06"; 
                        break;
                case "Jul": output+= "07"; 
                        break;
                case "Aug": output+= "08"; 
                        break;
                case "Sep": output+= "09"; 
                        break;
                case "Oct": output+= "10"; 
                        break;
                case "Nov": output+= "11"; 
                        break;
                case "Dec": output+= "12"; 
                        break;
            default: break; 
                
        }
        output+= "-";
        if(date.length()==12)
        {
            output+= 0;
            output+= date.charAt(0); 
        }
        else if(date.length()==13)
            output+= date.substring(0,2); 
        
        return output;
    }
}
