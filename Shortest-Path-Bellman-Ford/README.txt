Shortest Path - Bellman Ford
--------------------------

Edge weights should be > 0, ie there should be no negative cycles

For each Vertice with Cost=inf,prev=undef
for starting node S set priority=0,prev=0

For ( 1...V-1 )

	for each Edge(u,v) -> E
	
		if Cost(E) > Cost(u) + weight(u,v)
			 Cost(E) = Cost(u) + weight(u,v)
			 Prev(v) = u
         
         end for

end for

To get the Shorted Path from A to any destination D
  Trace back from D to A in the array using prev(D)

Cost(D) gives the shortest path cost from A to D.


O(EV)
