
# Database Links Documentation

## SEBI Data
- **Database:** `sebi_data`
- **Collection:** `data`
- **MongoDB URI:**  
  ```
  mongodb+srv://guest:guest_pass@intellewings.enj2zjz.mongodb.net/?retryWrites=true&w=majority&appName=Intellewings
  ```

## IOSCO Data
- **Database:** `iosco_data`
- **Collection:** `notices`
- **MongoDB URI:**  
  ```
  mongodb+srv://guest:guest_pass@intellewings.enj2zjz.mongodb.net/?retryWrites=true&w=majority&appName=Intellewings
  ```

## INTERPOL Data
- **Database:** `interpol_data`
- **Collection:** `red_notices`
- **MongoDB URI:**  
  ```
  mongodb+srv://guest:guest_pass@intellewings.enj2zjz.mongodb.net/?retryWrites=true&w=majority&appName=Intellewings
  ```

## Example Python Access

```python
from pymongo import MongoClient

uri = "mongodb+srv://guest:guest_pass@intellewings.enj2zjz.mongodb.net/?retryWrites=true&w=majority&appName=Intellewings"
client = MongoClient(uri)

# Example: access SEBI data
db = client["sebi_data"]
collection = db["data"]
for doc in collection.find().limit(5):
    print(doc)
```

