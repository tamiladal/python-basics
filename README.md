
# Python Data Science Environment Overview

## 1. Python Environment Setup
To get started with Python for data science, install:
- **Python**: Download from [python.org](https://www.python.org/)
- **Anaconda (Recommended)**: Bundled with Python, Jupyter Notebook, Spyder, and key libraries.
- **IDE/Editors**: VSCode, PyCharm, Jupyter Notebook, or Spyder.

Check installation:
```bash
python --version
pip --version
```

## 2. Spyder vs Notebook vs VSCode

| Feature        | Spyder                     | Jupyter Notebook          | VSCode                        |
|----------------|----------------------------|----------------------------|-------------------------------|
| Best for       | Scientific workflows       | Exploratory analysis       | Development + Data Science   |
| UI             | MATLAB-like                | Browser-based              | Modern code editor            |
| Code Execution | Script-based               | Cell-by-cell               | Script/cell-based             |
| Version Control| Basic                      | Limited                    | Git integration               |
| Extensions     | Limited                    | Extensive via JupyterLab   | Many via Marketplace          |

**Recommendation**: Use **Jupyter Notebook** for experimentation, **Spyder** for analytics, and **VSCode** for full-scale development.

## 3. Virtual Environment
Virtual environments allow isolated Python setups per project.

### Create Environment
```bash
python -m venv env_name
```

### Activate
- Windows:
  ```bash
  .\env_name\Scripts\activate
  ```
- macOS/Linux:
  ```bash
  source env_name/bin/activate
  ```

### Deactivate
```bash
deactivate
```

## 4. Packages - Libraries
Use `pip` or `conda` to install packages.

### Examples:
```bash
pip install pandas numpy matplotlib seaborn
```

- **pandas**: Data manipulation
- **numpy**: Numerical operations
- **matplotlib/seaborn**: Visualization
- **scikit-learn**: Machine learning

### Check installed packages:
```bash
pip list
```

## 5. Pandas
Powerful library for data analysis.

### Common Uses:
```python
import pandas as pd

df = pd.read_csv('data.csv')  # Load data
df.head()                     # View top rows
df.describe()                 # Summary stats
df['column'].value_counts()  # Count values
```

- **DataFrames**: 2D tabular structure
- **Series**: Single column/row of data

## 6. NumPy
Efficient array operations.

```python
import numpy as np

arr = np.array([1, 2, 3])
matrix = np.array([[1, 2], [3, 4]])

np.mean(arr)
np.reshape(matrix, (1, 4))
```

- Useful for scientific computations
- Basis for many other libraries

## 7. Datetime
Work with date and time objects.

```python
import datetime as dt

now = dt.datetime.now()
dt.datetime.strptime('2023-12-25', '%Y-%m-%d')
dt.timedelta(days=7)  # Duration
```

Also useful in Pandas:
```python
df['date'] = pd.to_datetime(df['date'])
df['year'] = df['date'].dt.year
```

---

**Note**: Always document your environment with `requirements.txt` or `environment.yml` for reproducibility.
