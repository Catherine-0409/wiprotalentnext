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

program 5 - isPrime?

import java.io.*;
import  java.util.*;
class UserMainCode
{
 public int isPrime(int input1){
  int count=0;
 for(int i=2;i<=Math.sqrt(input1);i++)
{
 if(input1%i==0)
     count++;
}
if(count==0)
 return 2;
 else
return 1;
 }
}

program 6 - FACTORIAL of a number

import java.io.*;
import  java.util.*;
class UserMainCode
{
 public int nFactorial(int input1){
  int fact=1;
for(int i=1;i<=input1;i++)
 {
fact=fact*i;
 }
return fact;
 }
}

program 7 - nth Fibonacci

import java.io.*;
import  java.util.*;
class UserMainCode
{
 public long nthFibonacci(int input1){
 if(input1==1)
 return 0;
if(input1==2)
 return 1;
 else
 return nthFibonacci(input1-1)+nthFibonacci(input1-2);
 }
}

program 8 - Nth Prime

import java.io.*;
import  java.util.*;
class UserMainCode
{
 public int NthPrime(int input1){
       int count=0,pcount=0,i;
  for(i=2;i<=100000;i++)
  {
   count=0;
   for(int j=2;j<=Math.sqrt(i);j++)
   {
    if(i%j==0)
     count++;
   }
   if(count==0)
    pcount++;
   if(pcount==input1)
    break;
  }
  return i; 
}}
