
# Python Dictionary Practice Solutions

## Problem 1: Create a Custom User Profile
- **Problem:** Write a function that accepts a dictionary of user information and returns a formatted profile string that includes the user's name, age, and location.

```python
def create_profile(user_data):
    return f"Name: {user_data['name']}, Age: {user_data['age']}, Location: {user_data['location']}"

# Example usage:
user = {'name': 'Ahad', 'age': 18, 'location': 'Sialkot'}
print(create_profile(user))
```
Output:

```yaml
Copy code
Name: Ahad, Age: 18, Location: Sialkot
```

---
# Python Dictionary Practice Solutions

## Problem 2: Merge and Filter Dictionaries
- **Problem:** Write a function that merges two dictionaries and filters out any key-value pairs where the value is an empty string.

```python
def merge_and_filter(dict1, dict2):
    merged = {**dict1, **dict2}
    return {key: value for key, value in merged.items() if value != ""}

# Example usage:
dict1 = {'name': 'Ahad', 'age': ''}
dict2 = {'location': 'Sialkot', 'occupation': 'Developer'}
print(merge_and_filter(dict1, dict2))
```
Output:

```python
Copy code
{'name': 'Ahad', 'location': 'Sialkot', 'occupation': 'Developer'}
```

---

## Problem 3: Count Word Frequency
- **Problem:** Write a program that uses a dictionary comprehension to count the frequency of each word in a given sentence.

```python
def word_frequency(sentence):
    words = sentence.split()
    return {word: words.count(word) for word in set(words)}

# Example usage:
sentence = "hello world hello python"
print(word_frequency(sentence))
```
Output:

```arduino
Copy code
{'hello': 2, 'world': 1, 'python': 1}
```

---
## Problem 4: Flatten a Nested Dictionary
- **Problem:** Write a program that flattens a nested dictionary using dictionary comprehension.

```python
def flatten_dict(d):
    return {f"{key}_{subkey}": subvalue for key, value in d.items() for subkey, subvalue in value.items()}

# Example usage:
nested_dict = {'user': {'name': 'Ahad', 'age': 18}, 'address': {'city': 'Sialkot', 'country': 'Pakistan'}}
print(flatten_dict(nested_dict))
```
Output:

```arduino
Copy code
{'user_name': 'Ahad', 'user_age': 18, 'address_city': 'Sialkot', 'address_country': 'Pakistan'}
```

---
## Problem 5: Advanced Dictionary Unpacking with Conflict Handling

- **Problem:** Write a function that merges multiple dictionaries using dictionary unpacking and handles conflicting keys by summing their values.

```python
def merge_and_sum(*dicts):
    merged = {}
    for d in dicts:
        for key, value in d.items():
            merged[key] = merged.get(key, 0) + value
    return merged

# Example usage:
dict1 = {'a': 1, 'b': 2}
dict2 = {'a': 3, 'c': 4}
dict3 = {'b': 1, 'd': 5}
print(merge_and_sum(dict1, dict2, dict3))
```
Output:

```css
Copy code
{'a': 4, 'b': 3, 'c': 4, 'd': 5}
```

---
