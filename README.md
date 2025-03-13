# Research Paper Fetcher

This Python script fetches research papers from PubMed based on a given query and filters them to find papers with at least one author affiliated with a pharmaceutical or biotech company. The results are saved to a CSV file.

## Features

- Fetches research papers from the **PubMed API**.
- Filters papers where at least one author is affiliated with a **pharmaceutical or biotech company**.
- Outputs results as a **CSV file**.
- Supports execution in **Jupyter Notebook** and as a standalone script.
- **Logging enabled** for debugging.

## Installation

### Prerequisites

Make sure you have **Python 3.x** installed along with the following dependencies:

```sh
pip install requests
```

## Usage

### **Running in Jupyter Notebook**

The script is designed to run smoothly in Jupyter. Just **copy and paste the script** into a Jupyter Notebook cell and execute it.

- The query is manually set inside the script:
  ```python
  query = "cancer research"  # Change this to your desired query
  filename = "results.csv"    # Set filename or None to print results
  debug_mode = False          # Set to True for debugging
  ```
- It automatically fetches and processes the research papers.
- The results are saved in **results.csv** in the same directory.

### **Running as a Standalone Script**

Run the script from the command line as follows:

```sh
python script.py "cancer research" -f results.csv
```

### **Checking Results**

To find the generated CSV file:

```python
import os
print(os.listdir())  # Lists all files in the current directory
```

If using **Google Colab**, download the file using:

```python
from google.colab import files
files.download("results.csv")
```

## Output Format

The CSV file contains the following columns:

| PubmedID | Title | Publication Date | Non-academic Authors | Company Affiliations |
| -------- | ----- | ---------------- | -------------------- | -------------------- |

## Error Handling

- If PubMed API fails, the script **logs errors** and retries.
- Handles **missing affiliations** properly.

## Debugging

To enable debug mode, set `debug_mode = True` inside the script or use `-d` in the CLI:

```sh
python script.py "diabetes research" -d
```

## Pushing to GitHub

Follow these steps to push your project to GitHub:

### **1. Initialize a Git Repository**
Navigate to your project folder and run:

```sh
git init
```

### **2. Add Files to the Repository**
```sh
git add .
```

### **3. Commit the Changes**
```sh
git commit -m "Initial commit"
```

### **4. Create a New GitHub Repository**
- Go to [GitHub](https://github.com/) and create a new repository.
- Copy the repository URL.

### **5. Link Local Repo to GitHub**
Replace `<your-repository-url>` with your actual GitHub repository link:

```sh
git remote add origin <your-repository-url>
```

### **6. Push Your Code to GitHub**
```sh
git branch -M main
git push -u origin main
```

Now, your code is successfully pushed to GitHub!

## License

This project is open-source and free to use.

## Author

Developed by Sanjivani.

