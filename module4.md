# wiprotalentnext
program 1 - Is N an exact multiple of M?

import java.io.*;
import  java.util.*;
class UserMainCode{
public int isMultiple(int input1,int input2){ 

if(input1==0 || input2==0) 

   return 3; 

else if(input1%input2==0)   

   return 2; 

else 

   return 1;

}}

program 2 - Of the given 5 numbers, How many are even?

import java.io.*;
import  java.util.*;
class UserMainCode{ 

public int countEvens(int input1,int input2,int input3,int input4,int input5){

 int count=0;  
if(input1%2==0)  
 count++;
 if(input2%2==0)   
    count++;  
if(input3%2==0)  
   count++;  
if(input4%2==0)   
   count++;  
if(input5%2==0)   
  count++;  

return count; 

}}

program 3 - Of the given 5 numbers, How many are odd?

import java.io.*;

import  java.util.*;

class UserMainCode{ 

public int countEvens(int input1,int input2,int input3,int input4,int input5){  

  int count=0;  
    if(input1%2!=0)   
       count++;  

     if(input2%2!=0)   
       count++;  
     
     if(input3%2!=0)   
        count++;
  
     if(input4%2!=0)   
       count++;  
     if(input5%2!=0)   
       count++;  
    
     return count; 

    }}
    
    program 4 - Of the given 5 numbers, How many are even or odd?
    
    import java.io.*;
import  java.util.*;
class UserMainCode
{
 public int countEvensOdds(int input1,int input2,int input3,int input4,int input5,String input6){
  int count=0;
  if(input1%2==0)
   count++;
  if(input2%2==0)
   count++;
  if(input3%2==0)
   count++;
  if(input4%2==0)
   count++;
  if(input5%2==0)
   count++;
  if(input6.equals("even"))
   return count;
  else
   return 5-count;
 }

}
