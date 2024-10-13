import requests

# URL of the JSON data
url = 'https://ps99-economy-bucket.s3.us-west-1.amazonaws.com/data_rng.json'

# Fetch the data from the URL
response = requests.get(url)
data = response.json()

# Convert JSON data into the desired list format
formatted_list = [f"{item[1]['id']} / {item[2]}" for item in data]

# Display the formatted list
for entry in formatted_list:
    print(entry)
