# Setting up PostgreSQL in VS Code with .ipynb

## Setting up PostgreSQL for use in Jupyter Notebook

### Install and Setup VS Code
- Install VS Code
- Install [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- Install Jupyter Notebook from [here](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) 

### Create a Virtual Environment
- Create a virtual environmetn using `python3 -m venv env_name`
- Activate it using `source env_name/bin/activate`

### Setting up kernel for Jupyter notebook
- `pip install ipykernel`
- `python -m ipykernel install --user --name=kernel_name --display-name="Kernel Dispay Name`

### Installing packages
- `pip install ipython-sql`
- `pip install sqlalchemy`
- `pip install psycopg2-binary`

### Connecting with PostgreSQL database
- Create .ipynb file
- Choose **Jupyter Kernel** in *Select Kernel* and select the kernel created above
- Run the following commands in top cell 
    - `%load_ext sql` 
    - `%sql postgresql://username:password@ip_adress/db_name`
