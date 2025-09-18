#DSA
Author: Striver
Source: YT

So in recursion basically we are going to call same function inside the function itself. And we will be having a base case depending on which recursion is going to end

Basically till code travels function inside a function everything is storred in stack memory and only ends when function is completely executed.

There are basically 2 ways to implement it

1) Forward propagation
	Task -> Recursive fn -> propagate -> base condition -> return answer
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250804095913.png)
	1,2,3,4,5
	
2) Back propagation
	Recursive fn -> propagate -> base condition -> task -> compute and return at each back prop
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250804095818.png)
	5,4,3,2,1


6/8/25

Practised recursions
1) Parameterised recursion problems
	Here the computation done inside the parameters itself like
	
	f(i, sum ) {
		f( i , sum+i)
		return;
	}
	
2) Function recursion problems
	Here function does the computation and return output as required
	f(i ) {
		sum=i+ f( i-1 )
		return sum;
	}

Functional recursions
1. Factorial
2. Reverse an array
	swap (i , n-i-1);  i++;  till i>=n/2
3. Palindrome

---
## References

1. Striver DSA