#include<stdio.h>
int main()
{

int n,i,flag,j,temp;
printf("enter the size of array: ");
scanf("%d",&n);
int a[n];
printf("\n elements of array:\n");
for(i=0;i<n;i++)
{
scanf("%d",&a[i]);
}
for (i=0;i<n-1;i++)
{
flag = 0;
for(j=0;j<n-1;j++)
{
if(a[j]>a[j+1])
{
temp = a[j];
a[j] = a[j+1];
a[j+1] = temp;
flag = 1;
}
}
if(flag==0)
{
break;
}

}
printf("sorted array is : ");
for(i=0;i<n;i++)
{
printf("%d\t",a[i]);
}
return 0;
}
