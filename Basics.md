Here is a basic template of a sqlite3 process.


```python
import sqlite3

db = sqlite3.connect(':memory:')

cursor = db.cursor()

# Python sqlite3 executions here

db.commit()
db.close()

```

A SQL statement can be executed by using the execute method from the cursor.

```python

cursor.execute('''
    CREATE TABLE Customers(id INTEGER PRIMARY KEY, name TEXT,
                       phone TEXT, email TEXT unique, address TEXT);
''')

```

