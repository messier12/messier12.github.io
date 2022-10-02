This problem is solved by Nehemy Davis Suryanto 5023221004 from TB04
## Too lazy to write the problem description
Do this pattern..
### Format Input
Integer less than 100, more than 0
### Format Output
pattern
### Example Input 1
```
3
```
### Example Output 1
```
  #    #    #
 ###  ###  ###
###############
```
### Example Input 1
```
5
```
### Example Output 1
```
    #        #        #        #        #
   ###      ###      ###      ###      ###
  #####    #####    #####    #####    #####
 #######  #######  #######  #######  #######
#############################################
```


### Solution by Nehemy Davis Suryanto
```c
#include <stdio.h>
#include <stdlib.h>

void print_satu_pyramid(i) {
  int row, space, hashtag, n;
  for (row = 1; row <= i; row++) {
    for (n = 0; n < i; n++) {
      int mathspace = i - row;
      int mathhashtag = (2 * row) - 1;
        // print spaces
        for (space = 1; space <= mathspace; space++)
        {
        printf(" ");
        }
        // print hashtag
        for (hashtag = 1; hashtag <= mathhashtag; hashtag++)
        {
        printf("#");
        }
        //print spaces again so that the next pyramid is well separated (fixing the cursor)
        for (space = 1; space <= mathspace; space++)
        {
        printf(" ");
        }
    }
    printf("\n");
  }
}

int main() {
  int i;
  scanf("%d", &i);
  if(i>0 && i<100)
    {
    print_satu_pyramid(i);
    }
  return 0;
}

```