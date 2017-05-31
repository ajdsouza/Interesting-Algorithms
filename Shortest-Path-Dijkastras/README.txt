Shortest Path - Dijkastras
--------------------------

Greedy Algorithm, Edge weights should be > 0

A heap is an ordered tree, where every parent child follow the same order
A Priority Queue, is a Queue where element with highest(or lowest) priority is
dequed first. A Priority Queue can be implemented using a Fibonacci Heap ( log
N for dequeing the element with the lowest priority)


Initialize a PQ adding each Vertice with Priority=inf,prev=undef
for starting node S set priority=0,prev=0

while ( A = Dequeue From PQ )

	for B ( each vertex B connected to A)

		if Cost(A)+cost(A,B) is lower than its current priority
			reduce its prority to  Cost(A)+cost(A,B)
			prev(B) = A
         
         end for

end while


To get the Shorted Path from A to any destination D
  Trace back from D to A in the array using prev(D)

Cost(D) gives the shortest path cost from A to D.


With Fibonaci Heap
O((E+V) log V)

With just a linked List
O(V^2)
