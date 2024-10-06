<h1>Module 1</h1>
<p>This module is about exploring and manipulating data structures within Python including: </p>
<ul>
    <li>Python lists</li>
    <li>Python dictionaries</li>
    <li>Other Python data structures: tuples and sets</li>
    <li>JSON objects and files</li>
</ul>

This notebook contains the end of module exercise used to practice skills.
This included importing a CSV file using the DictReader function in Python, and converting the data source to a Python dictionary for manipulation.
Once manipulation was complete, I exported the data to a separate JSON file using the `json.dump()` command.

Below gives a quick summary of the key data manipulation when using JSON in Python.

<strong>Python Dictionary to JSON object</strong>
```python
import json

# Dictionary to JSON string
data = {'name':'John', 'age':30}
json_data = json.dumps(data)

# JSON string to Python Dictionary
json_str = '{"name":"John", "age":30}'
data = json.loads(json_str)
```

<strong>Python List to JSON array</strong>
```python
import json

# Python list to JSON array
data = [1, 2, 3] 
json_data = json.dumps(data)

# JSON array to Python list
json_str = '[1, 2, 3]'
data = json.loads(json_str)
```

<strong>Python dict to JSON file</strong>
```python
import json

# Write Python dict to JSON file
data = {'name':'John'}
with open('data.json','w') as f:
  json.dump(data, f)
  
# Read JSON file to Python dict  
with open('data.json') as f:
  data = json.load(f)

# verify files exist
import os
file_exists = os.path.exists('data.json')
print("Verifying if data.json file exists:", file_exists)
```