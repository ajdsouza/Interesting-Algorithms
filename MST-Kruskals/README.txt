Minimum Spanning Tree - Kruskals
--------------------------------

Greedy Algorithm

A Disjoint set (Union-Find, Merge-Find) Data Structure keeps track of the set
am element belongs to. 



Initialize by adding all vertices to  its own in a Disjoint Set

Sort all edges by weight into ESorted

X = {}
For next Edge(u,v) in ESorted

	if find(u) ne find(v) ( they are in different sets)
		add edge(u,v) to X
		union(v,u)  ( union the set containing u with the set containing v)

end for


MST is X


Sort all the edges by cost Asc - ( O(ElogV) ) - ESorted
