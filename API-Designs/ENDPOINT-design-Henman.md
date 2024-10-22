1. GET /recipes

Purpose: Retrieve a list of recipes.

Required Data:

    Pagination parameters (optional):
        page: The page number of results to retrieve.
        limit: The number of results per page.

Returned Data:

    A list of recipes, each containing:
        recipe_id
        title
        user_id
        ingredients
        instructions
        prep_time

Database Query:

    SELECT * FROM Recipe LIMIT :limit OFFSET (:page - 1) * :limit;

2. POST /recipes

Purpose: Create a new recipe.

Required Data:

    Request body (JSON):
        title: String (required)
        user_id: Integer (required)
        ingredients: String (required)
        instructions: String (required)
        prep_time: Integer (required)

Returned Data:

    The created recipe object, including recipe_id.

Database Query:

    INSERT INTO Recipe (title, user_id, ingredients, instructions, prep_time)
    VALUES (:title, :user_id, :ingredients, :instructions, :prep_time);

3. PUT /recipes/{id}

Purpose: Update an existing recipe.

Required Data:

    Path variable:
        id: Integer (required)
    Request body (JSON):
        title: String (optional)
        ingredients: String (optional)
        instructions: String (optional)
        prep_time: Integer (optional)
       
Returned Data:

  The updated recipe object.

Database Query:

    UPDATE Recipe
    SET title = COALESCE(:title, title),
      ingredients = COALESCE(:ingredients, ingredients),
      instructions = COALESCE(:instructions, instructions),
      prep_time = COALESCE(:prep_time, prep_time),
    WHERE recipe_id = :id;

4. DELETE /recipes/{id}

Purpose: Delete an existing recipe.

Required Data:

    Path variable:
        id: Integer (required)

Returned Data:

    A success message: "Successfully deleted recipe."

Database Query:

    DELETE FROM Recipe WHERE recipe_id = :id;
