# wiprotalentnext

program 1 - Is Palindrome Number?

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int isPalinNum(int input1){
String str=Integer.toString(input1);
        int len=str.length();
        String str1="";
        for(int i=len-1;i>=0;i--)
        {
            str1+=str.charAt(i);
        }
        if(str.equals(str1))
        return 2;
        else
        return 1;
    }
}

program 2 - Is Palindrome possible?

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int isPalinNumPossible(int input1){
String str=Integer.toString(input1);
        int count[] = new int[256];
Arrays.fill(count, 0); // to initialize all values to zero
        for (int i = 0; i < str.length(); i++)
          count[(int)(str.charAt(i))]++;
        int odd = 0;
        for (int i = 0; i < 256; i++)
        {
           if ((count[i] & 1) == 1)
            odd++;
          if (odd > 1)
            return 1;
        }
        return 2;
    }
}

program 3 - Create PIN using three given input numbers

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int createPIN(int input1,int input2, int input3){
int arr[]={input1,input2,input3};
    int max=0,min;
    double sum=0.0;
    double place=1.0;
    int num;
    for(int i=0;i<3;i++)
    {
        num=arr[i];
        while(num!=0)
        {
          int r=num%10;
            if(r>max)
                max=r;
            num=num/10;
        }
    }
    for(int i=0;i<3;i++)
    {
         min=99;
          for(int j=0;j<3;j++)
          {
              int rem=arr[j]%10;
              if(rem<min)
                min=rem;
                arr[j]/=10;
          }
          sum=(min+(sum/place));
          sum*=place;
          place*=10;
    }
      return (int)(max*1000+sum);
    }
}
}
}

program 4 -Weight of a hill pattern

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int totalHillWeight(int input1, int input2, int input3){
        int sum=0;
        for(int i=0;i<input1;i++)
        {
            for(int j=0;j<=i;j++)
            {
                sum+=input2;
            }
            input2+=input3;
        }
        return sum;
    }
}

program 5 - Read second word and change to Uppercase

import java.io.*;
import  java.util.*;
class UserMainCode{

public String secondWordUpperCase(String input1){

String strArray[] = input1.split(" ");        

String stt="LESS";        

if(strArray.length==1) {            

return stt;        

}        

return strArray[1].toUpperCase();   

 }}
 
 program 6 - isPalindrome
 
 import java.io.*;
import  java.util.*;
class UserMainCode
{
public int isPalindrome(String input1){
String str=input1.toLowerCase();
        String str1="";
        for(int i=str.length()-1;i>=0;i--)
        {
            str1+=str.charAt(i);
        }
        if(str.equals(str1))
        return 2;
        else
        return 1;
    }
}

program 7 - Weight of String

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int weightOfString(String input1,int input2)
{
String str=input1.toUpperCase();
        int sum=0;
        for(int i=0;i<input1.length();i++)
        {
          if(input2==0)
          {
      if(str.charAt(i)=='A' || str.charAt(i)=='E' ||str.charAt(i)=='I' || str.charAt(i)=='O' || str.charAt(i)=='U' || !Character.isLetter(str.charAt(i)))
              {
                  continue;
              }
              else
              {
                  int a=str.charAt(i)-64;
                  sum+=a;
              }
          }
          else
          {
              if(!Character.isLetter(str.charAt(i)))
                  continue;
              else
              {
                  int a=str.charAt(i)-64;
                  sum+=a;
              }
          }
        }
        return sum;
    }
}

program 8 - Most Frequent Digit

import java.io.*;
import  java.util.*;
class UserMainCode
{
public int MostFrequentDigit(int input1, int input2, int input3, int input4){
int arr[]={input1,input2,input3,input4};
        int temp[]=new int[10];
        int num;
        for(int i=0;i<arr.length;i++)
        {   num=arr[i];
            while(num!=0)
            {
                int n=num%10;
                temp[n]++;
                num/=10;
            }
        }
        int max=-1;
        int x=0;
        for(int i=0;i<temp.length;i++)
        {
            if(temp[i]>=max)
            {
                max=temp[i];
                x=i;
            }
        }
    return x;
    }
}
