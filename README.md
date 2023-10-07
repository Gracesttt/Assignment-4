# Assignment-4
#include <stdio.h>
#include <math.h>

int main()
{
    int a,b,c;
    float x1,x2;
    
    printf("Enter a b c");
    scanf("%d %d %d",&a,&b,&c);
    puts("Root of the equation");
    
    switch(a){
        case 1: printf("x^2"); break;
        case 0: break;
        case -1: printf("-x^2"); break;
        default: printf("%dx^2",a);
    }
    
    if (b>0 && a==0){}
    else if(b>0) printf("+");
    
    switch(b){
        case 1: printf("x"); break;
        case 0: break;
        case -1: printf("-x"); break;
        default: printf("%dx",b);
    }
    
    if ((a!=0 || b!=0) && c>0) printf("+");
    if(c!=0) printf("%d",c);
    puts("=0");
    
 
    switch(c){
        case 0: break;
        case 1: printf("1"); break;
        case -1: printf("-1"); break;
    }
   
    float sq;
    
    sq=b*b-4*a*c;
    
    if(a==0){
        if(b!=0)
           printf("The answer is %.2f\n",-(float)c/b);
        else printf("No solution\n"); 
    }
    
    else if(sq>0){
        x1=(-b + sqrt(sq)) / (2 * a);
        x2=(-b - sqrt(sq)) / (2 * a);
        printf("Answer is x1=%.2f,x2=%.2f\n",x1,x2);
    }
    
    else if(sq==0){
        x1=-b/(2*a);
        printf("Answer is x1=x2=%.2f",x1);
    } 
    
    else if(sq<0) printf("No solution");
    
    
   return 0;
    
}   
        
