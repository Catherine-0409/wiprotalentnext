# wiprotalentnext
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
