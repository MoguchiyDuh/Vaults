---
tags:
  - programming
  - sql
related:
  - '[[00 - Programming MOC]]'
---
## Basic Syntax
```sql
SELECT column1, column2
FROM table_name
WHERE condition
ORDER BY column1 ASC/DESC;
```

---
## Common Clause
- **SELECT**: Specifies columns to retrieve
- **FROM**: Defines source table(s)
- **WHERE**: Filters rows based on conditions
- **JOIN**: Combines rows from multiple tables
- **GROUP BY**: Groups rows sharing property
- **HAVING**: Filters groups
- **ORDER BY**: Sorts result set

---
## Join Types
```sql
-- INNER JOIN (default)
SELECT * FROM table_a a
INNER JOIN table_b b ON a.id = b.a_id;
-- LEFT JOIN
SELECT * FROM table_a a
LEFT JOIN table_b b ON a.id = b.a_id;
-- RIGHT JOIN  
SELECT * FROM table_a a
RIGHT JOIN table_b b ON a.id = b.a_id;
-- FULL OUTER JOIN
SELECT * FROM table_a a
FULL OUTER JOIN table_b b ON a.id = b.a_id;
```

---
## Aggregation Functions
```sql
SELECT 
    COUNT(*),
    AVG(column),
    SUM(column),
    MAX(column),
    MIN(column)
FROM table_name
GROUP BY category_column;
```

---
## Subqueries
```sql
-- In WHERE clause
SELECT name FROM users
WHERE id IN (SELECT user_id FROM orders);
-- Correlated subquery
SELECT name, (SELECT COUNT(*) FROM orders WHERE user_id = users.id)
FROM users;
```

---
## CREATE
```sql
-- Create table
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    email VARCHAR(100) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    is_active BOOLEAN DEFAULT TRUE
);
-- Create table with foreign key
CREATE TABLE orders (
    id SERIAL PRIMARY KEY,
    user_id INTEGER REFERENCES users(id),
    amount DECIMAL(10,2),
    order_date DATE
);
```

---
## ALTER
```sql
-- Add column
ALTER TABLE users ADD COLUMN last_login TIMESTAMP;
-- Drop column  
ALTER TABLE users DROP COLUMN is_active;
-- Modify column type
ALTER TABLE users ALTER COLUMN email TYPE VARCHAR(150);
-- Add constraint
ALTER TABLE users ADD CONSTRAINT email_unique UNIQUE (email);
-- Drop constraint
ALTER TABLE users DROP CONSTRAINT email_unique;
-- Rename column
ALTER TABLE users RENAME COLUMN username TO user_name;
```

---
## UPDATE
```sql
-- Basic update
UPDATE users SET last_login = CURRENT_TIMESTAMP WHERE id = 1;
-- Update multiple columns
UPDATE users SET last_login = CURRENT_TIMESTAMP, is_active = FALSE WHERE id = 2;
-- Update with join
UPDATE orders 
SET amount = amount * 1.1 
FROM users 
WHERE orders.user_id = users.id AND users.created_at < '2024-01-01';
-- Conditional update with CASE
UPDATE products 
SET price = CASE 
    WHEN category = 'premium' THEN price * 1.2
    ELSE price * 1.1
END;
```

---
## DELETE
```sql
-- Delete specific rows
DELETE FROM users WHERE is_active = FALSE;
-- Delete with join
DELETE FROM orders 
USING users 
WHERE orders.user_id = users.id AND users.created_at < '2020-01-01';
-- Delete all rows (truncate faster for full table)
TRUNCATE TABLE audit_logs;
```

---
## DROP
```sql
-- Drop table
DROP TABLE temp_data;
-- Drop table if exists
DROP TABLE IF EXISTS deprecated_table;
-- Drop database
DROP DATABASE old_database;
```

---
## INSERT
```sql
-- Basic insert
INSERT INTO users (username, email) VALUES ('john_doe', 'john@example.com');
-- Multiple rows
INSERT INTO users (username, email) VALUES 
    ('jane_doe', 'jane@example.com'),
    ('bob_smith', 'bob@example.com');
-- Insert from select
INSERT INTO inactive_users (username, email)
SELECT username, email FROM users WHERE is_active = FALSE;
```

---
## Constraints Management
```sql
-- Add foreign key
ALTER TABLE orders ADD CONSTRAINT fk_user
FOREIGN KEY (user_id) REFERENCES users(id);
-- Add check constraint
ALTER TABLE products ADD CONSTRAINT positive_price
CHECK (price > 0);
-- Disable constraint temporarily
ALTER TABLE orders DISABLE TRIGGER ALL;
-- Bulk operations
ALTER TABLE orders ENABLE TRIGGER ALL;
```

---
## Index Operations
```sql
-- Create index
CREATE INDEX idx_users_email ON users(email);
CREATE UNIQUE INDEX idx_users_username ON users(username);
-- Drop index
DROP INDEX idx_users_email;
```

## See Also
- [[00 - Programming MOC]] - Programming overview
