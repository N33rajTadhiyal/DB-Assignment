Answer 1:
The product_category table and the product table have a one-to-many relationship in which a single product category can contain multiple products, but each product is only a part of one product category.

--------------------------------\***\*\*\*\*\*\*\***-----------------
Answer 2:

To ensure that each product in the "Product" table has a valid category assigned to it we can use Foreign key constraint between the 'product' table and 'product_catagory' table.

ALTER TABLE product
ADD CONSTRAINT fk_product_category
FOREIGN KEY (product_category_id)
REFERENCES product_category(id);
