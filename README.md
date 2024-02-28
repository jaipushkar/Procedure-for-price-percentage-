### SQL Stored Procedures for Data Comparison

1. **`QA_DATA_PERCENTAGE` Procedure:**
   - Calculates the percentage difference in price, altprice, pack, unit, and UOM between corresponding records in two tables.
   - Parameters:
     - `@newTableName`: Name of the newer table.
     - `@oldTableName`: Name of the older table.
     - `@productColumnName`: Name of the product identifier column.
     - `@brandColumnName`: Name of the brand identifier column.
   - Results are sorted by the percentage difference in price.

2. **`QA_CompareData` Procedure:**
   - Fetches specific columns from two tables where there's a difference in price for a given ZIP code.
   - Parameters:
     - `@tableName1`: Name of the first table.
     - `@tableName2`: Name of the second table.
     - `@productidColumn`: Product identifier column name.
     - `@sitecolumn`: Site identifier column name.
     - `@priceColumn`: Price column name.
     - `@zipColumn`: ZIP code column name.
   - Retrieves product IDs, old and new prices, description, and page image URLs for differing price records in the specified ZIP code.
