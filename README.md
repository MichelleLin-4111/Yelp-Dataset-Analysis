# Setup Instructions

## Prerequisites

1. **Install PostgreSQL:**  
   - On macOS, you can install PostgreSQL using Homebrew:  
     ```bash
     brew install postgresql
     ```  
   - After installation, start the PostgreSQL service with:  
     ```bash
     brew services start postgresql
     ```  
   - To stop the service, use:  
     ```bash
     brew services stop postgresql
     ```

2. **Install Python Dependencies:**  
   Ensure you have all the necessary Python packages by running:  
   ```bash
     pip install -r requirements.txt
   ```
3. **Additional Python Packages:**
    The following Python packages are required for the project and will be installed via `requirements.txt`:
    - psycopg3
    - random
    - random
    - json 

    If you encounter any missing packages, install them individually using:
    ```bash
     pip install <package_name>
    ```

## data
You don’t need to download the full Yelp dataset to run the queries in this project. The `code/sampling` notebook has already sampled data from the full Yelp dataset and saved it in the `sampled_data/ directory`.

If you want to explore the full Yelp dataset:
- **Data Source:** [Download the Yelp Open Dataset](https://www.yelp.com/dataset/download)
- **Documentation:** [Yelp Dataset Documentation](https://www.yelp.com/dataset/documentation/main)


# Repository Structure

```
.
├── README.md                     # Project documentation
├── writeup.md                    # Project writeup
├── code/                         # Code and scripts
│   ├── sampling/                 # Notebook to sample data from the full Yelp dataset
│   ├── schema_design/            # Scripts to create denormalized and normalized schemas
├── data/                         # Directory for the full Yelp dataset (excluded from Git)
├── queries/                      # SQL queries for analysis
│   ├── part1_normalization/      # Part 1: Analysis of normalized vs. denormalized data
│   ├── part2_query_optimization/ # Part 2: Query optimization analysis
│   ├── part3_data_analysis/      # Part 3: Exploratory and analytical queries
├── sampled_data/                 # Directory storing the sampled data used for analysis

```

**Note:** 
- It can be tricky to work with large files and git / GitHub. A `.gitignore` is setup to exclude many common large files, and **everything** inside `data/`is excluded.
- The sampled data stored in `sampled_data/` is sufficient to run all queries and analyses in this project.
---
