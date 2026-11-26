## # Relationship between objects
- Can relate two objects by relating the child object with the parent object.
- Object Manager > child object > field and relationships > new > lookup / master relationship > select the parent object to relate to > next .. > save.

### - Difference between Lookup and Master-Details relationship
1. **Master-Details :** Parent record is compulsary.</br>
   **Lookup :** Parent record is not compulsary.
2. Child gets deleted, if parent object is deleted.</br>
   Child doesn't get deleted even if parent object is deleted.
3. Only parent has the ownership.</br>
   Both child and the parent have independent owenership.
4. Only two relationship can be created.</br>
   40 relations can be created.
5. Can create roll up summary field.</br>
   We can't create the roll up summary field.

  Note:  __**We create Roll up summary field in the parent object.**__

### - What can we do with roll up summary field.
    - We can achieve 4 operations : Sum, Count, Max, Min.
  
### - What is junction object
    If one object have two master-detail relationships that particular object is known as junction object.
### - What is Self lookup
     If you are creating relationship of an object to itself then the object is said to be self related..

     
| Relationship Type   | Cardinality | Supported Objects          | Primary Use Case                            |
| :------------------ | :---------- | :------------------------- | :------------------------------------------ |
| Lookup              | 1:Many      | Standard & Custom          | Loose coupling, independent security        |
| Master-Detail       | 1:Many      | Parent: Any / Child: Custom| Tight coupling, roll-ups, inherited sharing |
| Many-to-Many        | Many:Many   | Junction: Custom Object    | Linking two objects in both directions      |
| Self                | 1:Many      | Same Standard or Custom    | Peer referrals or same-object hierarchies   |
| Hierarchical        | 1:1 / Tree  | `User` object only         | User approval chains and org charts         |
| External / Indirect | 1:Many      | Salesforce ↔ External Data | Integrating off-platform databases          |

