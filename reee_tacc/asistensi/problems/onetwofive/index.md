# One two five? Where is the rest of them?

Gura forgot about the number 3 and 4, so now she counts like this.
1 2 5 6 7 8 9 10 11 12 15 16 17 18 19 20 ... 28 29 50 51 52 55 ...

Your task is to convert Gura's counting to what it actually is.

The input is an integer less than 1000 greater than 0 and will not contain any 3 or 4.

## Example
### Input 1
```
5
```
### Output 1
```
3
```
### Input 2
```
20
```
### Output 2
```
16
```

## Solution by TB06
```c
#include <stdio.h>

int main()
{
    int G, R, X, Y;
    scanf("%d", &G);
     X=G/10;
     Y=G/100;
    if(G>=0&&G<3)
    {
        printf("%d", G);
    }
    else if(G>=5&&G<=1000&&G!=X*10+3&&G!=X*10+4&&!(G>=300&&G<=400))
    {
        if(G>=5&&G<=299)
        {
            if (G>=X*10+5&&G<X*10+10&&G<=29)
            {
                X=X+1;
                R=G-(2*X);
                printf("%d", R);
            }
            else if (G>=X*10&&G<=X*10+2&&G<=29)
            {
                R=G-(2*X);
                printf("%d", R);
            }
            else if (G>=Y*100+50&&G<=Y*100+99&&G>=X*10+5&&G<X*10+10&&G>29)
            {
                Y=Y+1;
                X=X+1;
                R=G-((2*X+20*Y)-4*Y);
                printf("%d", R);
            }
            else if (G>=Y*100+50&&G<=Y*100+99&&G>=X*10&&G<=X*10+2&&G>29)
            {
                Y=Y+1;
                R=G-((2*X+20*Y)-4*Y);
                printf("%d", R);
            }
            else if (G>=Y*100&&G<=Y*100+29&&G>=X*10+5&&G<X*10+10&&G>29)
            {
                X=X+1;
                R=G-((2*X+20*Y)-4*Y);
                printf("%d", R);
            }
            else if (G>=Y*100&&G<=Y*100+29&&G>=X*10&&G<=X*10+2&&G>29)
            {
                R=G-((2*X+20*Y)-4*Y);
                printf("%d", R);
            }
            else
            {
                printf("\nBukan Perhitungan Gura\n");
            }
        }
        else if(G>=500)
        {
            if (G>=Y*100+50&&G<=Y*100+99&&G>=X*10+5&&G<X*10+10)
            {
                Y=Y+1;
                X=X+1;
                R=G-((2*X+20*Y+128)-4*Y);
                printf("%d", R);
            }
            else if (G>=Y*100+50&&G<=Y*100+99&&G>=X*10&&G<=X*10+2)
            {
                Y=Y+1;
                R=G-((2*X+20*Y+128)-4*Y);
                printf("%d", R);
            }
            else if (G>=Y*100&&G<=Y*100+29&&G>=X*10+5&&G<X*10+10)
            {
                X=X+1;
                R=G-((2*X+20*Y+128)-4*Y);
                printf("%d", R);
            }
            else if (G>=Y*100&&G<=Y*100+29&&G>=X*10&&G<=X*10+2)
            {
                R=G-((2*X+20*Y+128)-4*Y);
                printf("%d", R);
            }
            else
            {
                printf("\nBukan Perhitungan Gura\n");
            }
        }
    }
    else
    {
        printf("\nBukan Perhitungan Gura\n");
    }
    return 0;
}
```