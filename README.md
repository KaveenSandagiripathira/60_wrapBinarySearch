# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

1. **What is meant by y = log2x ? Express its meaning in a.**
To what power should 2 be raised to in order to get x? 2^[?] = x

2. **What does its graph look like?**
log(x) is the inverse graph of e^x, the graph's domain is from (0, infinity) and it is montonically increasing but the rate of increase decreases as x increases.

3. Solution
   - State the problem
     - Return the index of the first instance of a give input in an ordered list through binary search.
   - State the Recursive Abstraction
     - Return the index of the first instanc of a given input in an ordered list half the size through binary search. 
   - Identify the parts of this solution that correspond to the six parts of a generalized recursive solution. 
     - Decision(s): if( low > hi), if( comparison == 0)
     - Solution To Base Case(s): return -2, return pageToCheck;
     - Solution To Recursive Case(s): 
       - return indexOf_recursive( findMe, low, pageToCheck -1) 
       - return indexOf_recursive( findMe, pageToCheck +1, hi)
    
