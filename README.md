# 2d-map-maker
Goal: Sparse graphical 2d coordinate system that quickly displays points-of-interest.

## research
### mapping points between coordinate systems

example set:
```
x=0,y=0  --->  x'=-1/2,y'=1/2
x=50,y=50  --->  x'=0,y'=0
x=100,y=100  --->  x'=1/2,y'=-1/2
```

solution:
```
x->ax+b, y->cy+d
```
Generally, start with the `(0,0)`, as that's easier: `0->b` and `0->d`, so `b=-1/2, d=1/2`  
And now, trivially, comes the rest `50->50a-1/2=0`; so, `a=1/100` and `50c+1/2=0` so `c=-1/100`  
Overall, use x->x/100-1/2 and y->-y/100+1/2

math from [stackoverflow](https://stackoverflow.com/questions/42682303/how-to-map-2d-point-from-one-coordinate-system-to-another), courtesy of @[Shahar Bental](https://stackoverflow.com/users/7343252/shahar-bental)
