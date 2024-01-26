Sorting algorithm

Article
Talk
Read
Edit
View history

Tools
From Wikipedia, the free encyclopedia

Merge sort
In computer science, a sorting algorithm is an algorithm that puts elements of a list into an order. The most frequently used orders are numerical order and lexicographical order, and either ascending or descending. Efficient sorting is important for optimizing the efficiency of other algorithms (such as search and merge algorithms) that require input data to be in sorted lists. Sorting is also often useful for canonicalizing data and for producing human-readable output.

Formally, the output of any sorting algorithm must satisfy two conditions:

The output is in monotonic order (each element is no smaller/larger than the previous element, according to the required order).
The output is a permutation (a reordering, yet retaining all of the original elements) of the input.
For optimum efficiency, the input data should be stored in a data structure which allows random access rather than one that allows only sequential access.

History and concepts
From the beginning of computing, the sorting problem has attracted a great deal of research, perhaps due to the complexity of solving it efficiently despite its simple, familiar statement. Among the authors of early sorting algorithms around 1951 was Betty Holberton, who worked on ENIAC and UNIVAC.[1][2] Bubble sort was analyzed as early as 1956.[3] Asymptotically optimal algorithms have been known since the mid-20th century – new algorithms are still being invented, with the widely used Timsort dating to 2002, and the library sort being first published in 2006.

Comparison sorting algorithms have a fundamental requirement of Ω(n log n) comparisons (some input sequences will require a multiple of n log n comparisons, where n is the number of elements in the array to be sorted). Algorithms not based on comparisons, such as counting sort, can have better performance.

Sorting algorithms are prevalent in introductory computer science classes, where the abundance of algorithms for the problem provides a gentle introduction to a variety of core algorithm concepts, such as big O notation, divide-and-conquer algorithms, data structures such as heaps and binary trees, randomized algorithms, best, worst and average case analysis, time–space tradeoffs, and upper and lower bounds.

Sorting small arrays optimally (in fewest comparisons and swaps) or fast (i.e. taking into account machine specific details) is still an open research problem, with solutions only known for very small arrays (<20 elements). Similarly optimal (by various definitions) sorting on a parallel machine is an open research topic.

Classification
Sorting algorithms can be classified by:

Computational complexity
Best, worst and average case behavior in terms of the size of the list. For typical serial sorting algorithms, good behavior is O(n log n), with parallel sort in O(log2 n), and bad behavior is O(n2). Ideal behavior for a serial sort is O(n), but this is not possible in the average case. Optimal parallel sorting is O(log n).
Swaps for "in-place" algorithms.
Memory usage (and use of other computer resources). In particular, some sorting algorithms are "in-place". Strictly, an in-place sort needs only O(1) memory beyond the items being sorted; sometimes O(log n) additional memory is considered "in-place".
Recursion: Some algorithms are either recursive or non-recursive, while others may be both (e.g., merge sort).
Stability: stable sorting algorithms maintain the relative order of records with equal keys (i.e., values).
Whether or not they are a comparison sort. A comparison sort examines the data only by comparing two elements with a comparison operator.
General method: insertion, exchange, selection, merging, etc. Exchange sorts include bubble sort and quicksort. Selection sorts include cycle sort and heapsort.
Whether the algorithm is serial or parallel. The remainder of this discussion almost exclusively concentrates upon serial algorithms and assumes serial operation.
Adaptability: Whether or not the presortedness of the input affects the running time. Algorithms that take this into account are known to be adaptive.
Online: An algorithm such as Insertion Sort that is online can sort a constant stream of input.
