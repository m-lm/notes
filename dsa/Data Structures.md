## Arrays

Arrays are possibly the most ubiquitous and intuitive data structure. The main benefit of using arrays is the constant-time access by index. This capability is thanks to fixed-length record sizes that allow direct calculation of the location in memory of the element. Since they consist purely of data in a contiguous layout, it is memory-efficient: no extraneous information like pointers or formatting are necessary and the size is often known up front, preventing unpredictable and sometimes wasteful resizing.

Physically, successive data accesses are based on memory locality and actually help speed of the access by leveraging fast caches on a computer's architecture.

However, one major downside of arrays is that it requires allocating memory upfront based on a fixed size. This forces precision on the part of the programmer, but makes it difficult to resize since it is inherently represented as a contiguous block in memory, rendering it static rather than dynamic.

Nowadays, many languages offer a dynamic version of an array. For example, in C++ they are known as vectors; in Java, as array lists. Python natively supports dynamic arrays with its list data type.

## Red-Black Trees

Red-black trees are a special variant of binary search trees which use an extra bit to store a color property for each of its nodes. This helps guarantee that no path from root to leaf is more than twice as long as any other, making the tree approximately balanced. Also, the leaves of red-black trees are understood to be NIL nodes.

Red-black trees have 5 important properties:
1. Every node is either red or black
2. The root is always black
3. Every leaf (NIL) node is black
4. If a node is red, its children are black
5. For each node, all paths from node to leaves contain same number of black nodes (black height).

Property 5 alludes to the concept of a tree's *black height*, which is the number of black nodes from the root of a subtree down to any of its leaves. Note that this includes the black NIL leaf nodes, but excludes the root node itself.