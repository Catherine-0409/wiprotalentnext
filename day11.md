# wiprotalentnext
program 1 - Find string code

import java.io.*;
import java.util.*;
class UserMainCode{
public int findStringCode(String input1){
String str=input1.toUpperCase();    
String word[]=str.split(" ");    
String value2="";    
for(int i=0;i<word.length;i++)    {     
int sum=0;     
for(int j=0;j<word[i].length()/2;j++)     {      
int first=word[i].charAt(j);      
int last=word[i].charAt(word[i].length()-1-j);       
sum+=Math.abs(first-last);     
}    
 if(word[i].length()%2!=0)     
sum+=(word[i].charAt(word[i].length()/2)-64);          
String value=Integer.toString(sum);         
  value2+=value;   
 }   
 return Integer.parseInt(value2);
 }}

program 2 - Get code through string

import java.io.*;
import java.util.*;
class UserMainCode{
public int getCodeThroughString(String input1){
String word[]=input1.split(" ");  
int sum=0;  
for(int i=0;i<word.length;i++)  
{          
sum+=word[i].length();  
}   
return (1 + (sum-1) %9); 
}}

program 3 - Add number string

import java.io.*;
import java.util.*;
class UserMainCode
{
public int addNumberString(String input1,String input2)
{
int carry=0;
  if(input1.length()<input2.length())
  {
    String temp="";
   temp=input1;
   input1=input2;
   input2=temp;
  }
  int len1=input1.length();
  int len2=input2.length();
  String str="";
  int j=len2-1;
  for(int i=0;i<len1;i++)
  {
   int a=Character.getNumericValue(input1.charAt(len1-1-i));
   int b=0;
   if(j>=0)
   {
    b=Character.getNumericValue(input2.charAt(j));
    j--;
   }
   int sum=a+b+carry;
   carry=sum/10;
   int init=sum%10;
   str=Integer.toString(init)+str;
   if(i==len1-1 && carry>0)
   {
              str=Integer.toString(carry)+str;
    }
  }
  return str;
 }
}

program 4 - simple encoded array

import java.io.*;
import java.util.*;
class UserMainCode
{
 public class Result
  {
    public final int output1;
    public final int output2;
public Result(int out1,int out2){
  output1=out1;
  output2=out2;
}}
  public Result findOriginalFirstAndSum(int[] input1,int input2){
int[] arr=new int[input2];
  arr[input2-1]=input1[input2-1];
  int sum=arr[input2-1];
  for(int i=input2-2;i>=0;i--)
        {
   arr[i]=input1[i]-arr[i+1];
   sum+=arr[i];
  }
         Result r1= new Result(arr[0],sum);
   return r1;
  }
    }
    
 program 5 - decreasing sequence
    
    class UserMainCode
{
public class Result{
 public final int output1;
 public final int output2;
 public Result(int out1,int out2)
 {
  output1=out1;
  output2=out2;
 }
}
public Result decreasingSeq(int[] input1,int input2)
{
 int c1=0,c2=0,max=0;
for(int i=0;i<input2-1;i++)
        {
            if(input1[i]>input1[i+1])
            {
                c1++;
            }
            if((input1[i]<input1[i+1] && c1!=0) || ((i==input2-2) && c1!=0))
            {
                if(max<c1)
                {
                    max=c1;
                }
                c2++;
                c1=0;
            }
        }
        max=max+1;
        if(c2==0)
        {
            max=0;
        }
        if(input2==0)
        {
            max=0;
            c2=0;
        }
        Result r1= new Result(c2,max);
        return r1;
}
}

program 6 - Most frequently occuring digit 

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int mostFrequentlyOccurringDigit(int[] input1,int input2)
{
               int[] arr=new int[10];
  for(int i=0;i<input2;i++)
  {
    while(input1[i]!=0){
    int rem=input1[i]%10;
    arr[rem]++;
    input1[i]/=10;
   }
 }
 int max=0;
 int higest_occur_number=0;
 for(int i=0;i<10;i++)
 {
  if(arr[i]>=max)
  {max=arr[i];
    higest_occur_number=i;
  }
 }
 return higest_occur_number;
}}

program 7 - Sum of power of digits

import java.io.*;
import  java.util.*;

class UserMainCode{  

public int sumOfPowerOfDigits(int input1){ 

double sum=0.0; 
String str=Integer.toString(input1);   
for(int i=0;i<str.length()-1;i++)  {   

 int a=Character.getNumericValue(str.charAt(i)); 
 int b=Character.getNumericValue(str.charAt(i+1));   
sum=sum + Math.pow(a, b);  
 } 
 return (int)sum+1; 
}}

program 8 - Sum of digits in cyclic

import java.io.*;

import  java.util.*;

class UserMainCode{

public int sumOfSumsOfDigits(int input1){             

String str=Integer.toString(input1); 

int sum=0; 
for(int i=0;i<str.length();i++)  {   
 for(int j=i;j<str.length();j++){   

int num=Character.getNumericValue(str.charAt(j));   

sum+=num;  
}} 

  return sum; 

}
