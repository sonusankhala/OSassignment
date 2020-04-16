// OSassignment
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
  File*fp=fopen("CPU_BURST.TXT","r");
  int bt[20],p[20],wt[20],tat[20],i=0,j,n=5,total=0,pos,temp;
  
