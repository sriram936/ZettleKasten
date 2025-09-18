
1) Primal problem f(x), g(x),h(x), with constraints
2) L(x,A) = f(x) + Ag(x)   (only 1 constraint, equality)
3) L(x,A) = f(x) + Aigi(x)  (many constraint, equality)
4)  L(x,A,v) = f(x) + Aigi(x) + vihi(x)  (many constraint, equality, inequality)
5) Langrangean dual function n dual problem used and try to solve
	1. Create lagrangean   L(x,A,v) = f(x) + Aigi(x) + vihi(x)
	2. create lagrangean fn   l(A,v) = min <sub>x</sub> (L(X,A,v))    (A>=0)
	3. L(X,A,v)  <= f(x)
	4.  l(A,v) = min <sub>x</sub> (L(X,A,v)) <= f(x)
	5.  l(A,v) <= f(x)   A>=0    (Satisfy either ur primal is  not convex)
	6. max( l(A,v) ) = f(x)  A>=0  (Satisfy only if ur primal f(x) is convex )
	7. Dual Problem : max( l(A,v) ) ,  A>=0
	8. Complementary slackness : Aigi(x*) = 0; since f(x*) + Aigi(x*) + vihi(x*) = f(x*) 
	9. KKT  Necessary Conditions  = all ur X*(Optimal sol) Local Minima  
		1. lagrangean differntiate wrt x = 0      deltaL = 0  Stationary
		2. Constraints  g(x)i<=0, hi(x)=0 given    Feasible Constrains
		3. (A>=0)     Positive Lagrangean Multiplier
		4. Aigi(x*) = 0
	10.  KKT  Sufficient Conditions  =  X* global minima
		1. Satisfy necessary condition and fi,gi,hi = differentiable+ convex