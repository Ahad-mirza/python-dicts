

Copy code
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
