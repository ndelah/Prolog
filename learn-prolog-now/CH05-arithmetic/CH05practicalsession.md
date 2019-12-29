# 5.6 Practical Session
 
# Exercise 1: create accMin


# Exercise 2: Create the scalar multiplier

```
scalmult(_,[],[]).
scalmult(A,[H|T],[Hnew|Tnew]):-
    Hnew is A * H,
    scalmult(A,T,Tnew).
```
    
	
## Exercise: Create a vector multiplier

```
accDot([],[],A,A).
accDot([H1|T1],[H2|T2],A,Result):-
    Anew is A + (H1*H2),
    accDot(T1,T2,Anew, Result).

dot(A,B,C):-
    accDot(A,B,0,C).```