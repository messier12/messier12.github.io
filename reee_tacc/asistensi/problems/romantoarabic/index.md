# Roman to arabic
What you need to do is simple, convert roman numerals to arabic.
I know this is kinda easy to google, but try doing it yourself.

btw, if you don't know how to read roman numerals, you should google it, i'm too lazy to describe it here.

The largest roman numerals possible is MMMCMXCIX
which is basically 3999.

## Examples
### Input 1
```
MMMCMXCIX
```
### Output 1
```
3999
```
### Input 2
```
DCLXVI
```
### Output 2
```
666
```

## Solution by Guardian Armananta TE32
```c
#include <stdio.h>
#include <string.h>

int indexOf(char);

// 7 roman symbols
char roman[] = "IVXLCDM";
int arabic[] = {1, 5, 10, 50, 100, 500, 1000};

int main(){
	int n = 0, i, j;
	char input[10];

	//input
	printf("");
	scanf("%s", &input);

	i = strlen(input) - 1;
	n += arabic[indexOf(input[i])];
	j = i;
	i--;

	while(i >= 0){
		if(indexOf(input[i]) >= indexOf(input[j])){
			n += arabic[indexOf(input[i])];
		}else{
			n -= arabic[indexOf(input[i])];
		}
		i--;
		j--;
	}

	//output
	printf("%d\n", n);
	return 0;
}

int indexOf(char c){
	int i;
	for(i = 0; i < 7; i++){
		if(roman[i] == c){
			return i;
		}
	}
	return -1;	//NOT FOUND
}
```