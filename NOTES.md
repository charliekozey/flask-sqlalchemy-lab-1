# Flask-SQLAlchemy Lab 1

## Key Concepts and Commands

- server
- database schema
- RESTful routing
- SQLAlchemy models
- migration (`flask db migrate`)
- upgrade (`flask db upgrade head`)
- flask shell commands
  - `.query()`
  - `.filter()`
  - `.filter_by()`
  - `.first()`
  - `.all()`
- serialization (`SerializerMixin`)
  
## Helpful tools

### SQLite (VSCode Extension)
Lets you view your database tables

### iPython
Interactive Python shell with syntax highlighting and other features
  
```sh
$ ipython -i filename.py
```

### Self-Quiz

- What are 3 different ways you can access your database entities?
  1. Open the database viewer using the SQLite VSCode extension
  2. Use `flask shell`:
        ```
        Python 3.8.13 (default, Oct 24 2022, 16:17:37) 
        [Clang 13.1.6 (clang-1316.0.21.2.5)] on darwin
        App: app
        Instance: /Users/charliekozey-flatiron/Code/phase_4_python/python-p4-v2-flask-sqlalchemy-lab-1/server/instance

        >>> Earthquake.query.all()

        [<Earthquake 1, 9.5, Chile, 1960>, <Earthquake 2, 9.2, Alaska, 1964>, <Earthquake 3, 8.6, Alaska, 1946>, <Earthquake 4, 8.5, Banda Sea, 1934>, <Earthquake 5, 8.4, Chile, 1922>]
        ```
  3. Use the `sqlite` CLI:
        ```
        $ sqlite3 instance/app.db

        SQLite version 3.37.0 2021-12-09 01:34:53
        Enter ".help" for usage hints.

        sqlite> SELECT * FROM earthquakes;

        1|9.5|Chile|1960
        2|9.2|Alaska|1964
        3|8.6|Alaska|1946
        4|8.5|Banda Sea|1934
        5|8.4|Chile|1922
        ```
2. What are `.filter()` and `.filter_by()`? What are their similarities and differences?

3. How can you set up and populate your database tables with Flask?