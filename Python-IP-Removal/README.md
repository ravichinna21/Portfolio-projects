# Automating IP Address Removal with Python
- **Date:** March 2025
- **Overview:** As a security professional at a health care company, I created a Python algorithm to automate the removal of IP addresses from an allow list based on a remove list, ensuring restricted content access is secure.
- **What I Did:**
  - Opened the "allow_list.txt" file in read mode using a `with` statement (`with open(import_file, "r") as file:`).
  - Read the file contents into a string using the `.read()` method and stored it in the `ip_addresses` variable.
  - Converted the `ip_addresses` string into a list using the `.split()` method to separate IP addresses.
  - Iterated through the `remove_list` using a `for` loop to check for IP addresses in the `ip_addresses` list.
  - Removed matching IP addresses from the `ip_addresses` list using the `.remove()` method with a conditional check to avoid errors.
  - Converted the updated `ip_addresses` list back into a string using the `.join()` method with `\n` as the separator.
  - Overwrote the "allow_list.txt" file with the updated list in write mode (`with open(import_file, "w") as file:`) using the `.write()` method.
- **Skills Used:**
  - Python programming (file handling, loops, string/list methods like `.read()`, `.split()`, `.join()`, `.remove()`).
  - Automation of security processes.
  - Attention to detail in managing access control.
- **Findings:**
  - The allow list contained IP addresses that were also in the remove list, indicating unauthorized access to restricted content.
  - Manual updates to the allow list were time-consuming and prone to errors.
- **Results:**
  - Automated the process of updating the allow list, ensuring only authorized IP addresses have access to restricted content.
  - Improved security by removing unauthorized IP addresses efficiently.
    ### Code Snippet
```python
import_file = "allow_list.txt"
remove_list = ["192.168.1.2", "10.0.0.5"]  # Example IPs

# Open and read the file
with open(import_file, "r") as file:
    ip_addresses = file.read()

# Convert string to list
ip_addresses = ip_addresses.split()

# Remove IPs from remove_list
for element in remove_list:
    if element in ip_addresses:
        ip_addresses.remove(element)

# Convert list back to string
ip_addresses = "\n".join(ip_addresses)

# Write updated list back to file
with open(import_file, "w") as file:
    file.write(ip_addresses)
