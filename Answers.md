## 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

Ans :
      The relationship between the "Product" and "Product_Category" entities in the provided diagram is typically represented as a one-to-many relationship. In this relationship:
      
      - One product category can have multiple products associated with it.
      - However, each product can belong to only one product category.
          
This relationship is implemented by using a foreign key in the "Product" table that references the primary key of the "Product_Category" table. This foreign key constraint ensures that each product is assigned to a valid product category. By establishing this relationship, it becomes easier to organize and categorize products, enabling efficient management and retrieval of information based on product categories.


## 2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
Ans :
      To ensure that each product in the "Product" table has a valid category assigned to it, we have to implement a foreign key constraint between the "category_id" column in the "Product" table and the primary key column in the "Product_Category" table. This foreign key constraint will enforce referential integrity, ensuring that every value entered into the "category_id" column of the "Product" table must already exist in the primary key column of the "Product_Category" table.
    
 we can ensure this:
1. Define the foreign key constraint during the creation of the "Product" table or alter the table to add the constraint later.
2. The foreign key constraint specifies that the "category_id" column in the "Product" table references the primary key column in the "Product_Category" table.
3. When inserting or updating data in the "Product" table, the database system will check if the value being inserted into the "category_id" column exists in the "Product_Category" table.
4. If the value exists, the operation will proceed successfully. If not, the database system will raise an error, preventing the insertion or update of invalid category IDs in the "Product" table.
