# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

## Answers

### Black - Box
To begin verifying the claim that the sorting algorithm runs in $O(n)$ time, I would start by testing the algorithm with random inputs of varying lengths. According to the claim, the algorithm should scale linearly with the size of the input. This means that the difference in time between sorting two input sizes should be proportional to the size difference. If the the time taken begins to waver by more than a constant factor (esspecially at large input sizes) I would then be able to assume that the claim that it runs in $O(n)$ time is false.

If it passed the earlier test with randomly sorted lists, I would then test the algorithm with sorted, near sorted, reverse sorted, and nearly reverse sorted lists of varying lengths. If this researchers claims are correct, then all of these should run in nearly identical run times as well as being identical to the randomly sorted lists. If they do not, then I would then again be able to assume that the claims that it runs in $O(n)$ time is false.


### Theoretical
Theoreticaly this is an impossible task. By the decision tree, there is atleast $n!$ leaves and by such tree will have a depth of atleast $\lceil{lg(n!)}\rceil$. As we covered in class (and by the Stirling Approximation) we get that $lg(n!) = n \cdot lg(n) \in \Theta (n \cdot log(n))$. As it is not possible for something to have both a theta bound of $\Theta (n \cdot log(n))$ and an O bound of $O(n)$, we can conclude that either the researcher's analysis is wrong or they did not do comparisions of two elements at a time.

## Sources

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.