# Pizza and Sosig
versi indonesia -> click [here](/reee_tacc/asistensi/problems/pizzasosig/index_id.html)
Arshad is a pizza chef in planet Vecashee. Today, he wants to create a pizza.

He began by shaping the dough to a perfect circle with diameter $D_{pizza}$ and placed it on a cartesian coordinate.

Now he wants to put Sosig (Sausage) with diameter $D_{sosig}$ on the dough. Arshad wants to do this with style. He picked a random coordinate, then throw the Sosig there. He however wants to know in advance, will the Sosig rest properly on the dough, partially rest on the dough, or not rest on the dough at all.

Arshad is a perfectionist and a skilled sharpshooter. The pizza dough he made and the Sosig he used is a perfect circle. His throw also never miss a target.

> Note
> If othe dough and the sosig only touching on their circumference, the sosig will be considered as not resting on the dough.
## Input Format
The input consist of 6 real numbers separated by space in the following order:

$D_{pizza}$ $D_{sosig}$ $X_{pizza}$ $Y_{pizza}$ $X_{sosig}$ $Y_{sosig}$

$D_{pizza}$ denotes the diameter of the pizza dough
$D_{sosig}$ denotes the diameter of the sosig.
$X_{pizza}$ $Y_{pizza}$ denotes the coordinate of the center of the pizza dough.
$X_{sosig}$ $Y_{sosig}$ denotes the coordinate of the center of the sosig target.

## Output Format
You must determine whether the sosig will rest on the dough, partially rest on the dough, or not rest on the dough at all.

If the sosig will rest on the dough, output:
```
Finally, some good f-ing good
```
If the sosig will partially rest on the dough, output:
```
You Idiot
```
If the sosig will not rest on the dough at all, output:
```
You Idiot Sandwich
```

## Examples
#### Input 1
```
4 1 0 0 1.5 0
```
#### Output 1
```
Finally, some good f-ing good
```
#### Input 2
```
3 3 1 1 -1 -1 
```
#### Output 2
```
You Idiot
```

#### Input 3
```
3 1 0 0 2.5 2.5
```
#### Output 3
```
You Idiot Sandwich
```

The figure below represent input 1, 2 and 3 respectively.
![example](example.png)
