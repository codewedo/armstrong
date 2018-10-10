# armstrong
#include<stdio.h>
#include<math.h>
int prime(int n)
{int i,z,j,flag=0;
 for(i=2;i<n;i++)
     if(n%i==0)
       break;
    if(i==n)
    {printf("%d IS A PRIME NO\n",n);
     for(j=1;j<=10;j++)
       {z=n*j;
       printf("%d\n",z);}
     }
}


int main()
{

  int n,i,z,j,temp,k,flag=0;

  printf("ENTER A NUMBER\n");
  scanf("%d",&n);
  temp=n;  /*Created new variable because in line 49  value of n changes to 0*/
  k=temp;  /*Created new variable because in line 49  value of n changes to 0*/


  printf("k=%d\n",k);
  printf("temp=%d\n",temp);

  /*for(i=2;i<n;i++)
    {if(n%i==0)
       break;}

  if(i==n)
    {printf("%d IS A PRIME NO\n",n);
     flag=1;}

 if(flag==1)
    for(j=1;j<=10;j++)
       {z=n*j;
       printf("%d\n",z);}
       */
 /*CALLING FUNCTION TO CHECK NO PRIME AND PRINTS MULTIPLICATION TABLE*/

 /* FIRST WE COUNT NO OF DIGIT IN GIVEN INPUT NUMBER*/
 int count=0,b=0,a,v;

 while(n>0)
 {n=n/10;
 count=count+1;}
 printf("%d\n",count);
 printf("n=%d",n);

 /*NOW WE CHECK THE NUMBER IS ARMSTTRONG OR NOT*/


 while(k!=0)
   {
    a=k%10;
    v=pow(a,count);
    b=b+v;
    k=k/10;        /*value of n change to 0*/
   }
   printf("b=%d\n",b);
   printf("a=%d\n",a);
 if(b==temp)
    printf("%d IS A ARMSTRONG",temp);
 else
    printf("%d IS NOT A ARMSTRONG",temp);
  return 0;
  }
