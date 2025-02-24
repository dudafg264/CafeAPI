# Cafe API

A simple REST API built with Flask and SQLAlchemy to manage a database of cafes. The API allows users to retrieve information about cafes, add new cafes, update coffee prices, and delete cafes.

## Features

- Retrieve a random cafe from the database.
- Get all cafes stored in the database.
- Search for cafes by location.
- Add a new cafe.
- Update the price of coffee at a specific cafe.
- Delete a cafe from the database.

## Technologies Used

- Python
- Flask
- Flask-SQLAlchemy
- SQLite

## Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/your-username/cafe-api.git
   cd cafe-api
   ```

2. Create and activate a virtual environment:

   ```sh
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate     # On Windows
   ```

3. Install dependencies:

   ```sh
   pip install -r requirements.txt
   ```

4. Run the application:

   ```sh
   python app.py
   ```

## API Endpoints

### Get a Random Cafe

**GET** `/random`

Returns a random cafe from the database.

### Get All Cafes

**GET** `/all`

Returns a list of all cafes in the database.

### Search for a Cafe by Location

**GET** `/search/<location>`

Returns a list of cafes matching the specified location.

### Add a New Cafe

**POST** `/add`

**Parameters (form-data):**
- `name` (str)
- `map_url` (str)
- `img_url` (str)
- `location` (str)
- `sockets` (bool)
- `toilet` (bool)
- `wifi` (bool)
- `calls` (bool)
- `seats` (str)
- `coffee_price` (str)

Returns a success message if the cafe is added successfully.

### Update Coffee Price

**PATCH** `/update-price/<cafe_id>?new_price=<price>`

Updates the coffee price of the specified cafe.

### Delete a Cafe

**DELETE** `/delete/<cafe_id>`

Deletes the cafe with the specified ID.