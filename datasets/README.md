# Sample Datasets for Power BI and Fabric Workshop

This directory contains sample datasets that you can use to practice building reports in Power BI and working with Microsoft Fabric.

## Available Datasets

### 1. Sales Data (sales-data.csv)

A sample dataset containing sales transactions with the following columns:
- **OrderID**: Unique identifier for each order
- **OrderDate**: Date when the order was placed
- **CustomerID**: Unique identifier for the customer
- **CustomerName**: Name of the customer
- **Product**: Product name
- **Category**: Product category
- **Quantity**: Number of units sold
- **UnitPrice**: Price per unit
- **TotalAmount**: Total transaction amount
- **Region**: Geographic region
- **SalesRep**: Sales representative name

**Use Cases:**
- Creating sales dashboards
- Time series analysis
- Customer segmentation
- Regional performance analysis

### 2. Employee Data (employee-data.csv)

A sample dataset containing employee information with the following columns:
- **EmployeeID**: Unique identifier for each employee
- **FirstName**: Employee's first name
- **LastName**: Employee's last name
- **Department**: Department name
- **Position**: Job title
- **HireDate**: Date of hire
- **Salary**: Annual salary
- **Manager**: Manager's name
- **Location**: Office location
- **PerformanceRating**: Performance rating (1-5)

**Use Cases:**
- HR analytics
- Organizational structure visualization
- Compensation analysis
- Performance tracking

### 3. Product Inventory (product-inventory.csv)

A sample dataset containing product inventory information with the following columns:
- **ProductID**: Unique identifier for each product
- **ProductName**: Name of the product
- **Category**: Product category
- **Supplier**: Supplier name
- **UnitsInStock**: Current stock level
- **ReorderLevel**: Minimum stock level before reorder
- **UnitPrice**: Price per unit
- **LastRestockDate**: Date of last restock
- **Warehouse**: Warehouse location

**Use Cases:**
- Inventory management dashboards
- Stock level monitoring
- Supplier performance analysis
- Reorder alerts

## How to Use These Datasets

### In Power BI Desktop

1. Open Power BI Desktop
2. Click "Get Data" > "Text/CSV"
3. Navigate to this datasets folder
4. Select the CSV file you want to use
5. Click "Load" or "Transform Data" to import

### In Microsoft Fabric

#### Using a Lakehouse

1. Create a new lakehouse in your Fabric workspace
2. Click "Get data" > "Upload files"
3. Select the CSV files from this directory
4. The files will be stored in OneLake

#### Using Data Pipelines

1. Create a new data pipeline
2. Add a "Copy data" activity
3. Set source as "File system" or "HTTP"
4. Point to these CSV files
5. Configure the destination (lakehouse, warehouse, etc.)

## Dataset Relationships

If you want to create a data model with relationships:

- **Sales Data** ↔ **Employee Data**: Join on SalesRep (Sales) to EmployeeID or Name (Employee)
- **Sales Data** ↔ **Product Inventory**: Join on Product (Sales) to ProductName (Inventory)

## Data Dictionary

For detailed information about each field and data types, see the individual dataset descriptions above.

## Practice Exercises

### Beginner Level

1. Create a simple bar chart showing total sales by region
2. Build a table showing employee count by department
3. Display current inventory levels by category

### Intermediate Level

1. Create a sales trend line chart by month
2. Build a matrix showing sales by category and region
3. Add slicers for date range and product category
4. Create calculated measures for Year-over-Year growth

### Advanced Level

1. Implement a star schema with dimension and fact tables
2. Create DAX measures for advanced calculations (running totals, percentage of total, etc.)
3. Build a complete dashboard with multiple pages
4. Add drill-through functionality for detailed analysis
5. Implement row-level security based on region

## Extending the Datasets

Feel free to:
- Modify the data to fit your learning needs
- Add additional columns
- Create related tables
- Generate more sample records
- Combine datasets for more complex scenarios

## Data Generation

These datasets are synthetically generated for educational purposes. All names, companies, and data are fictional and any resemblance to real entities is purely coincidental.

## License

These sample datasets are provided under the same MIT License as the repository. See the LICENSE file in the root directory for details.
