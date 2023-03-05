#include<stdio.h>
int main()
{
int p,q,m,n,k;
int cases;
scanf("%d",&cases);
while(cases--)
{
scanf("%d%d%d%d%d",&p,&q,&m,&n,&k);
int q1=0,q2=0;
int t=0;
int m1;
int i=0;
int j=0;
int planeland=0;
int planetakeoff=0;
int time[100000] = {0};
m1=m;
while(t<=k)
{
if(p) //when plane is moving in the air
{
p--;
planeland++;
time[i]=t;
i++;
t++;
q1++;
}
else //when there is no plane moving in air
{
if(q) //plane already waiting to take off since starting
{
q--;
planetakeoff++;
t++;
}
else // plane waiting to take off after landing
{
if(t >= (time[j]+n) && q1)
{
planetakeoff++;
q1--;
t++;
j++;
}
else
t++;
}
}
if(t==m1)
{
p++;
m1=m1+m;
}
}
q2=q+q1;
printf("\n %d %d %d %d\n",planeland,planetakeoff,p,q2);
}
return 0;
}
