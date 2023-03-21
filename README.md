# Pizza Restaurant API

This is an API for tracking pizza restaurants, where a user can perform CRUD operations on restaurants, pizzas, and restaurant pizzas. The API has three main resources, namely restaurants, pizzas, and restaurant_pizzas, which are related to each other through the following relationships:
* A Restaurant has many Pizzas through RestaurantPizza
* A Pizza has many Restaurants through RestaurantPizza
* A RestaurantPizza belongs to a Restaurant and belongs to a Pizza

# Technologies Used
 * Ruby 
 * Rails 
 * PostgreSQL database

 # Setup
To set up and run the API on your local machine, follow these steps:

1. Clone the repository and navigate to the project root directory.
git clone https://github.com/
cd 
2. Install dependencies
bundle install
3. Set up the database
rails db:migrate
rails db:seed
4. Start the server
rails server 
The server will start running at http://localhost:3000/

# Models 
The API has three models, namely Restaurant, Pizza, and RestaurantPizza, which are defined as follows:

# Restaurant
  * name: the name of the restaurant (string), required
  * address: the address of the restaurant (string), required
# Pizza
  * name: the name of the pizza (string), required
  * ingredients: the list of ingredients used in the pizza (string), required
# RestaurantPizza
  * price: the price of the pizza in the restaurant (integer), required, validation: must have a price between 1 and 30
  * restaurant_id: the ID of the restaurant that serves the pizza, required
  * pizza_id: the ID of the pizza that is served in the restaurant, required

 # Routes
The API has the following routes for performing CRUD operations on the resources:

Restaurants
GET /restaurants
<img src="images/Screenshot from 2023-03-21 14-49-51.png" alt="">

