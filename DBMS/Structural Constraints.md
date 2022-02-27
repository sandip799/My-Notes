# Structural Constraints of Relationship in ER Diagram
- To understand Structural Constraints, we must take a look at Cardinality Ratios and Participation Constraints.
- **Cardinality Ratio of Relationship**:-
	- The entities are denoted by rectangle and relationships by diamond.
	- ![[Pasted image 20210820004325.png]]
	- There are numbers (represented by M and N) written above the lines which connect relationships and entities. These are called cardinality ratios. These represent the maximum number of entities that can be associated with each other through relationship, R.
- **Types Of Cardinality**-
	- There can be 4 types of cardinality –
	- ![[Pasted image 20210820004711.png]]
	 1.  **One-to-one (1:1) –**  
    When one entity in each entity set takes part at most once in the relationship, the cardinality is one-to-one.
	1.  **One-to-many (1: N) –**  
    If entities in the first entity set take part in the relationship set at most once and entities in the second entity set take part many times (at least twice), the cardinality is said to be one-to-many.
	1.  **Many-to-one (N:1) –**  
    If entities in the first entity set take part in the relationship set many times (at least twice), while entities in the second entity set take part at most once, the cardinality is said to be many-to-one.
	1.  **Many-to-many (N: N) –**  
    The cardinality is said to be many to many if entities in both the entity sets take part many times (at least twice) in the relationship set.