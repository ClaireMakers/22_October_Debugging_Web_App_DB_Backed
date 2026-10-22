# Debugging Database Backed Apps

## Learning Objectives

- Explain why we might encounter new bugs now we're working with databases
- Debug database backed applications methodically
- Learn about database backed applications through debugging one

## Setup

To get set up, follow these steps...

### 1. Set up the virtual environment
```
; python -m venv databases-starter-venv
```

### 2. Activate the virtual environment
```
; source databases-starter-venv/bin/activate 
```


### 3. Install dependencies
```
(databases-starter-venv); pip install -r requirements.txt
```

> Read below if you see an error with `python_full_version`

### 4. Create the database
```
(databases-starter-venv); createdb db_debugging_workshop
```

### 5. Run the tests - see below if you have any issues
```
(databases-starter-venv); pytest
```
> Some tests should fail but if you get an `ModuleNotFoundErrorort` error, see below.

### 6. Run the app
```
(databases-starter-venv); python app.py
```

> If you run the tests again after running the app, you might notice the number of failing tests has changed :)

<br>
<details>
  <summary>I get a <code>ModuleNotFoundError: No module named 'psycopg'</code></summary>
  <br>
If, after activating your <code>venv</code> and installing dependencies, you see this error when running <code>pytest</code>, please deactivate and reactivate your <code>venv</code>. This should solve the problem - if not, contact your coach.
</details>
