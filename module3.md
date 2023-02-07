# wiprotalentnext
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
