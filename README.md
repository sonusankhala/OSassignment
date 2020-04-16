// OSassignment
//answer of question no.9


#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
  File*fp=fopen("CPU_BURST.TXT","r");
  int bt[20],p[20],wt[20],tat[20],i=0,j,n=5,total=0,pos,temp;
  float avg_wt,avg_tat;
  pritf("\n Reading CPU_BURST.TXT file\n ");
  while((getc(fp))!=EOF)
  {
    fscanf(fp,"%d",$bt[i]);
    if(bt[i]>0)
    {
      p[i]=i+1;
      i++;
    }
  }
  n=i;
  for(i=0;i<n;i++)
  {
    pos=i;
    for(j=i+1;j<n;j++)
    {
      if(bt[j]<bt[pos])
        pos=j;
    }
    temp=bt[i];
    bt[i]=bt[pos];
    bt[pos]=temp;
    temp=p[i];
    p[i]=p[pos];
    p[pos]=temp;
 
  }
  wt[0]=0;
  //calculate avg waiting time
   for(i=1;i<n;i++)
   {
    wt[i]=0;
     for(j=0;j<i;j++)
     {
      wt[i]+=bt[j];
     }
     total+=wt[i];
   }
   // calculate avg trunaround time
   avg_wt=(float)taotal/n;
   total=0;
   printf("\nprocess\t  Burst Time \t waiting time\t  trunaround time");
     for(i=1;i<n;i++)
     {
      tat[i]=bt[i]+wt[i];
      total+=tat[i];
      printf("\np%d\t\t  %dt\t  %d\t\t\t%d ,p[i],bt[i],wt[i],tat[i]");
     }
     avg_tat=(float)total/n;
     printf("\n\nAverage waiting time=%f,avg_wt");
      printf("\nAverage trunaround  time=%f\n,avg_tat");
      return 0;
  
