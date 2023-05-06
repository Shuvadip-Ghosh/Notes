### Importing Flask
```python
from flask import Flask, render_template, redirect, request
```

### Important imports
```markdown
- Flask : to initialte the app
- render_template : to render any .html file in the templates directory
- redirect : to redirect from any route
- request : to acess any data from post request made to the server and other things.
```

### Flask Boilerplate or minimal app
```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"
    
if __name__ == "__main__":
	app.run(debug=True, host="0.0.0.0", port=5000)
```

### Creating a route
```python
#to handle only get request
@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"

#to handle only post request
@app.route("/",methods = ['POST'])
def hello_world():
    return "<p>Hello, World!</p>"
    
#to handle both get and post requests
@app.route("/",methods = ['GET', 'POST'])
def hello_world():
    return "<p>Hello, World!</p>"
```

# Templates and Static directory
You obviously don't want to only serve static text shown above you would like to have an html file with cool css and javascript.  
```markdown
1. templates
2. static
```
  
Just Create the two folders listed below as it is written because flask wants it that way. Store .html files in templates and css and js files in the static folder.  
  
**Note: Any file kept in the static folder is served as a part of the website don't keep and important files like config files in it or it can be downloaded by the users.**

### Rendering a Template from a route
```python
# rendering file_name.html file from the templates directory
@app.route("/")
def hello_world():
    return render_template("file_name.html")
```

### Redirecting
```python
return redirect('https://google.com')
```

# Request
Mainly used for getting the type of request and forms data when you are not using flask forms and using simple html forms. But has other uses also.
```python
if request.method =="POST":
	var = request.form.get('name_attribute_of_label_in_html')
```

```html
<input type="email" name="name_attribute_of_label_in_html" class="form-control" id="emailid" required autofocus>
```

**It has other uses like it can get the user-agent of your user**
```python
print(str(request.user_agent))
```
# Databases

## Installing Flask Sqlalchemy 

```bash
pip install Flask-SQLAlchemy
```

### Importing 
```python
from flask_sqlalchemy import SQLAlchemy
from sqlalchemy.exc import IntegrityError #helps in dealing with errors
```

### Setting Database URI
```python
#if you are using a .db file
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///db_name.db'
#if you are using mysql
#localhost
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://username:password@localhost/db_name' 
#cloud
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://username:password@hostname:port/db_name'
```

**Note : if you are encountering any error such as **
```yaml
ImportError: No module named MySQLdb
``` 
Then do the following**
```bash
pip install pymysql
```

```python
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql+pymysql://username:password@hostname:port/db_name'
```

## Initialization

This is to initialise the database add this after the app is declared
```python
db = SQLAlchemy(app)
```

## Creating a Model or Table 
```python
class TableName(db.Model): 
    column_1 = db.Column(db.Integer, primary_key=True)
    column_2 = db.Column(db.String(80), nullable=False)
    column_3 = db.Column(db.String(12), nullable=False)
    column_4 = db.Column(db.DateTime, default=datetime.datetime.utcnow)

#below part only required once
with app.app_context():
    db.create_all()
```

## Adding a row in the table

```python
try:
	data_to_add = TableName(column_2=data_2, column_3= data_3, column_4=data_4)
    db.session.add(data_to_add)
    db.session.commit()
except IntegrityError:
	db.session.rollback()
```

## Deleting a row
```python
try:
	data_to_del = TableName(column_2=data_2, column_3= data_3, column_4=data_4)
    db.session.delete(data_to_del)
    db.session.commit()
except IntegrityError:
	db.session.rollback()
```

## Getting Data

```python
#all
variable = TableName.query.all()
#filter First
variable = TableName.query.filter_by().first()
```

## Updating a row
```python
try:
	up_data = TableName.query.filter_by(column_1 = required_parameter).first()
	up_data.column_2 = new_data
    db.session.commit()
except IntegrityError:
	db.session.rollback()
```


## Official documentation
Visit Here : [Flask Official Docs]([Welcome to Flask — Flask Documentation (2.3.x) (palletsprojects.com)](https://flask.palletsprojects.com/en/latest/))
Visit Here : [Flask Request Official Docs](https://tedboy.github.io/flask/generated/generated/flask.Request.html))
Visit here : [Flask Sqlalchemy Official Docs]([Flask-SQLAlchemy — Flask-SQLAlchemy Documentation (3.1.x) (palletsprojects.com)](https://flask-sqlalchemy.palletsprojects.com/en/latest/))
