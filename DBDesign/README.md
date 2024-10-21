# Start DB Container:
- Verify if Docker is installed and running. Clone repository in local machine.
- Navigate into the project's folder and start the docker container: `docker compose up`
- Access the container: `docker exec -it cookbook`

# Validate DB Configuration:
- To connect, use DB:
  - username: user
  - password: password
- Once connected, do some checks like: `SELECT * FROM User`

# SQL Scripts:
- Breakdown of the scripts and what they do:
  - View All Recipes: Retrieve all recipes from the Recipe table
  - Track Recipe Likes: Count the number of likes each recipe has received
  - Count Recipe Comments: Count how many comments have been made on each recipe.
  - Count User Comments: Count the amount of comments each user has made.
  - Track Likes and Favorites: The relationship between recipe likes and favorites which shows how many likes and favorites each recipe has. 
