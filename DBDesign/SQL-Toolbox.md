# View Recipes (View All recipes)
    SELECT * FROM Recipe

# Track Occurances (How many times recipes are liked)
    SELECT r.recipeID, r.title, COUNT(l.likeID) as likeCount
    FROM Recipe r
    LEFT JOIN Like l ON r.recipeID = l.recipeID
    GROUP BY r.recipeID, r.title;

# Query Count (Amounts of comments in recipe)
    SELECT r.recipeID, r.title, COUNT(c.commentID) AS commentCount
    FROM Recipe r
    LEFT JOIN Comment c ON r.recipeID = c.recipeID
    GROUP BY r.recipeID, r.title;

# Query Count(Amount of comments a user has made)
    SELECT u.userName, COUNT(c.commentID) AS commentCount
    FROM User u
    LEFT JOIN Comment c ON u.userID = c.userID
    GROUP BY u.userName;

# Query Between Multiple Tables (How Favorite and Like relate)
    SELECT r.recipeID, r.title,
      COUNT(l.likeID) AS likeCount,
      COUNT(f.favoriteID) AS favoriteCount
    FROM Recipe r
    LEFT JOIN Like l ON r.recipeID = l.recipeID
    LEFT JOIN Favorite f ON r.recipeID = f.recipeID
    GROUP BY r.recipeID, r.title;

