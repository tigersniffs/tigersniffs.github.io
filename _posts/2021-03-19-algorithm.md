class Solution {
    public String addBinary(String a, String b) {
        
       int carry=0; 
        
       StringBuilder a1 = new StringBuilder(a);
       StringBuilder b1 = new StringBuilder(b);
       StringBuilder c = new StringBuilder();
        
       a1.reverse();
       b1.reverse(); 
        
       int i=0,sum; 
       while(a.length() >i || b.length() > i){
           sum = carry; 
           if(i<a.length()) sum += a1.charAt(i)-'0';
           if(i<b.length()) sum += b1.charAt(i)-'0';
           
           if(sum == 0) {
               carry = 0;
               c.append(sum);
           }
           
           if(sum == 1){
               carry = 0;
               c.append(sum);
           }
           
           if(sum == 2){
               carry = 1;
               c.append("0");
           }
           if(sum == 3){
               carry = 1;
               c.append("1");
           }
           i++;
       }
        
       if(carry == 1){
           c.append(carry);
       }
        
        return c.reverse().toString();
    }

}


leetcode addbinary
