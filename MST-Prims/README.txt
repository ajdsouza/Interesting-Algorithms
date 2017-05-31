MST - Prims
--------------------------

This is a similar implementation to Dijkastras MST with subtle changes instead
of choosing the vertice based on Cost(A) + Cost(A,B), we look at only the
minimum edge cost of Cost(A,B)

Greedy Algorithm, 

A heap is an ordered tree, where every parent child follow the same order
A Priority Queue, is a Queue where element with highest(or lowest) priority is
dequed first. A Priority Queue can be implemented using a Fibonacci Heap ( log
N for dequeing the element with the lowest priority)


Initialize a PQ adding each Vertice with Priority=inf,prev=undef
for starting node S set priority=0,prev=0

while ( A = Dequeue From PQ )

	for B ( each vertex B connected to A)

		if cost(A,B) is lower than its current priority
			reduce its prority to  cost(A,B)
			prev(B) = A
         
         end for

end while

prev has the MST


With Fibonaci Heap
O((E+V)log V)

With just a linked List
O(V^2)

Prim is prefered over Kruskal when edges are dense
