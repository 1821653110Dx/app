# for
## eval $1^2 + 2^2 + 3^2 + 4^2 + 5^2$
```matlab
sum = 0 ;
for n = 1 : 5 ;	% for each n in [1..5]
	sum += n^2 ;
end ;
```
## eval $\sum^5_{i=1}i!$
```matlab
%% eval sum = SUM(i!,1,5)
sum = 0 ;
for i = 1:5 ;	% for each i in [1 .. 5]
	%% eval p = i!
	p = 1 ;
	for j = 1 : i ;	% for each j in [1 .. i]
		p *= j ;
	end

	sum += p ;
end ;
```
# if
```matlab
a = 100 ;
b = 20 ;
if a > b ;
	'True' ;
else ;
	'False' ;
```
# switch
```matlab
grade = 'b' ;
switch grade ;	% switch by grade
	case 'b' ;
		a = 1 ;
	case 'c' ;
		a = 2 ;
	otherse ;
		a = 3 ;
end
```
