# 6.3 Exercises
## Exercise 6.1

```
doubled(L,Doubled):-
    append(L,L,Doubled).
```

## Exercise 6.2

```
palindrome(X):-
    reverse(X,X).
```

## Exercise 6.3

**Without using append**
```
toptail([H|T],CorrectOrder):-
    reverse(T,[_|B]),
    reverse(B,CorrectOrder).
	```

**Using append**
```
toptail(Inlist,Outlist):-
    append([_|Outlist],[_],Inlist).
```

## Exercise 6.4

**Using reverse **
last(List,X):-
    reverse(List,[X|_]).
	

## 6.5

prefix(P,L) :- append(P,_,L).
suffix(S,L) :- append(_,S,L).
sublist(SubL,L) :- suffix(S,L), prefix(SubL,S).

zebra(ZebraOwner):-
    Street = [_,_,_],
    member(house(red,englishman,_),Street),
    member(house(_,spanish,jaguar),Street),
    member(house(_,ZebraOwner,zebra),Street),
    sublist([house(_,_,snail),house(_,japanese,_)],Street),
    sublist([house(_,_,snail),house(blue,_,_)],Street).
	
	
**Mistakes**
You can simply add the ZebraOwner in the member house. 
No needto make the japanese and snail separate member facts. Already implied by the sublist