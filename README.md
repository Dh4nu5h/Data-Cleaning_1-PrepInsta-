Data Cleaning Project Documentation
Dataset Overview
This project focuses on cleaning and standardizing a dataset containing employment-related information. The cleaned dataset includes information about job positions, including age requirements, salary offerings, company ratings, locations, establishment dates, and application processes.
Columns in the Dataset:

Age: Employee/position age requirement (numerical)
Salary: Compensation offered (in thousands)
Rating: Company rating (scale: 0-10)
Location: Geographic location of the position
Established: Company establishment year
Easy Apply: Boolean indicator for application process

Data Cleaning Process
1. Missing Values

Identified and handled missing values in the dataset
Rating column contained some 0.0 values which might indicate missing ratings
No NULL values remained in the final dataset

2. Data Type Standardization

Age: Integer
Salary: Float (in thousands)
Rating: Float (up to 1 decimal place)
Location: String (standardized format)
Established: Integer (year)
Easy Apply: Boolean

3. Outlier Treatment

Age range: 13-66 years
Salary range: 29.5K-94.5K
Rating range: 0.0-7.8
Kept outliers with valid business justification

4. Data Standardization
Location Standardization

Standardized location format to "City Country" format
Three main locations in the dataset:

India In
New York Ny
Australia Aus



Salary Formatting

Converted all salary values to floating-point numbers
Standardized to thousands (K) format
Range from 29.5K to 94.5K

Rating Normalization

Maintained ratings on a scale of 0-10
One instance of calculated average rating (3.528571)
Preserved zero ratings as they might indicate new listings

5. Data Integrity Checks

Verified establishment years (1932-2020)
Validated age ranges for positions
Ensured location consistency
Confirmed boolean values for Easy Apply

Dataset Statistics

Total Records: 29
Unique Locations: 3
Salary Brackets: 29.5K-94.5K
Establishment Year Range: 1932-2020
Age Range: 13-66 years

Usage Notes

The dataset is ready for analytical purposes
All columns have been standardized and cleaned
No missing values in the final dataset
Boolean values are represented as True/False

Future Improvements

Further standardization of location names
Implement additional validation for age requirements
Consider normalizing ratings to a standard scale
Add currency indicators for salary values

Dependencies

Python 3.x
Pandas Library
NumPy Library

File Structure
Copyproject/
│
├── data/
│   ├── final_cleaned_dataset.csv    # Cleaned dataset
│   └── dataset1.csv         # Original dataset
│
└── README.md                        # This documentation
