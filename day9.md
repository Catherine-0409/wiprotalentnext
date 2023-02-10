# wiprotalentnext
program 1 count primes

import java.io.*; 
import java.util.*;
class UserMainCode{     
  public int countPrimesInRange(int input1, int input2){      
 
   int count=0;        
   int pcount=0;         
  for(int i=input1;i<=input2;i++){   
      
  count=0;        
for(int j=2;j<=Math.sqrt(i);j++) {       
 
if(i%j==0)         
  count++;       
  }       
if(count==0)         
  pcount++;     
  } 
  return count; 
  }}
  
program 2 - all digits count 

import java.io*;
import java.util.*;
class UserMainCode
{
   public int allDigitsCount(int input1)
{
   String str=Integer.toString(input1);
   return str.length();
  }
}

program 3 - uniquedigits count

import java.io.*;
import  java.util.*;

class UserMainCode{

public int uniqueDigitsCount(int input1){

String str = Integer.toString(input1);

int len=str.length();   

int count=0;

for(int i=0;i<len-1;i++){           

for(int j=i+1;j<len;j++){               

if(str.charAt(i)==str.charAt(j)) {           

count++;                     
break;                 
}} 
 }       
  return len-count;   
}}

program 4 - non repeat digits count

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int nonRepeatDigitsCount(int input1){
String str = Integer.toString(input1);
int len=str.length();
int count=0,pcount=0;
for(int i=0;i<len;i++)
{
          count=0;
for(int j=0;j<len;j++)
{
                if(i!=j)
if(str.charAt(i)==str.charAt(j))
{
count++;
break;
}
}
            if(count==0)
              pcount++;
}
return pcount;
}
}

program 5 - digit sum 

import java.io.*;
import  java.util.*;
class UserMainCode
{
                public int digitSum(int input1){
                                int neg=input1;
                                if(input1<0)
                                {
                                                input1*=-1;
                                }
                                int len=Integer.toString(input1).length();
                                if(len==1)
                                {
                                                if(neg<0)
                                                return input1*-1;
                                                else
                                                                return input1;
                                }
                                else
                                {
                                                int sum=0;
                                while(input1!=0)
                                {
                                                int rem=input1%10;
                                                sum+=rem;
                                                input1/=10;
                                }
                                                if(neg<0)
                                                                return digitSum(sum*-1);
                                                else
                                                                return digitSum(sum);
                }}
}

program 6 - even digits sum

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int EvenDigitsSum(int inpu1){
int sum=0;
while(input1!=0)
{
int n=input1%10;
if(n%2==0)
sum+=n;
input1/=10; 
}
return sum;
}

program 7 - odd digits sum 

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int OddDigitsSum(int inpu1){
int sum=0;
while(input1!=0)
{
int n=input1%10;
if(n%2!=0)
sum+=n;
input1/=10; 
}
return sum;
}

program 8 - even or odd digits sum

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int OddDigitsSum(int input1,String input2){
      int sum=0;
        if(input2.equals("even"))
        {
while(input1!=0)
    {
 int n=input1%10;
 if(n%2==0)
    sum+=n;
  input1/=10; 
    }
        }
        else
        {
    while(input1!=0)
    {
     int n=input1%10;
   if(n%2!=0)
    sum+=n;
  input1/=10; 
    }
        }
       return sum;
    }
}
