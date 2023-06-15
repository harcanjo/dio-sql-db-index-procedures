# Parte 2 - Utilização de procedures para manipulação de dados em Banco de Dados 

Exemplo SQL:
```sql
DELIMITER //
CREATE PROCEDURE data_manipulation(IN action INT, IN id INT, IN new_value VARCHAR(255))
BEGIN
    CASE action
        WHEN 1 THEN
            SELECT * FROM mytable WHERE mycolumn = id;
        WHEN 2 THEN
            UPDATE mytable SET mycolumn = new_value WHERE mycolumn = id;
        WHEN 3 THEN
            DELETE FROM mytable WHERE mycolumn = id;
    END CASE;
END //
DELIMITER ;
```
Exemplo Universidade:
```sql
-- Script for university database
USE university;

DELIMITER //
CREATE PROCEDURE university_data_manipulation(IN action INT, IN id INT, IN new_value VARCHAR(255))
BEGIN
    CASE action
        WHEN 1 THEN
            SELECT * FROM students WHERE student_id = id;
        WHEN 2 THEN
            UPDATE students SET student_name = new_value WHERE student_id = id;
        WHEN 3 THEN
            DELETE FROM students WHERE student_id = id;
    END CASE;
END //
DELIMITER ;
```

Exemplo E-commerce:
```sql
-- Script for e-commerce database
USE ecommerce;

DELIMITER //
CREATE PROCEDURE ecommerce_data_manipulation(IN action INT, IN id INT, IN new_value VARCHAR(255))
BEGIN
    CASE action
        WHEN 1 THEN
            SELECT * FROM products WHERE product_id = id;
        WHEN 2 THEN
            UPDATE products SET product_name = new_value WHERE product_id = id;
        WHEN 3 THEN
            DELETE FROM products WHERE product_id = id;
    END CASE;
END //
DELIMITER ;
```