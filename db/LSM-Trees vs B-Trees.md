#database-internals

### Reads vs Writes

What are the differences between B-Trees and LSM-Trees? They are both commonly used data structures that form the foundation for database storage engines. The main difference between them is that B-Trees are *read-optimized*, meaning 

LSM-Trees, on the other hand, are *write-optimized*. This is primarily due to its use of appends rather than writes-in-place. To write in place, a node in the tree must be first looked up, which itself is a nontrivial task. Then the write can take place. This is why B-Trees are generally slower for write-based workloads. LSM-Trees directly append to structures that become immutable. Thus, there is no need to discriminately search for a specific node to update and change the structure of the tree, as new nodes are directly appended via cleverly designed data structures.
