**Landing / Main application page**

- Goal:
- This will be the main homepage of our app.

User Flow:
  - 1: User's purpose:
   - The first part of the user flow decides what the user is aiming to do on our application.
   - They can scroll through new and top recipe posts.
   - Post a new recipe.
   - Create an account or login if they haven't already.
   - Or search for a desired recipe.

**Search:**

![cookbookcreateflow](cookbookcreateflow.png)

- Goal:
- This will allow users to create a new entity or a post in the application.
User Flow:
  - 1: 'Create' Button:
    - Create Button will be clearly displayed to simplify it for users.
    - User clicks the 'Create' button to show the 'Create' page for the users to begin inputting content. After, click 'Create' when done.
 - 2: Decision Node:
   - Did they create the recipe they wanted? Does it have the tags for the system to know what category it belongs?
   - Verification:
     - If yes, save and post the content. Will display message for user as a verification that the content was created: "Recipe posted!"
     - If no, show error message and ask user to enter valid content. Ex: "Title required", "Tags required".
 - 3: Post-Submission:
   - After creating post, it will refresh to the user's page where it lists their existing posts and will add the newly created recipe.
  
Wireframe:
- Layout:
  - Title: Placed at the top-left corner with placeholder (TITLE)
  - Date Create: Placed at the top-right corner with placeholder (Date Created)
  - Upload: Under title but above ingredients and recipe (Image of Dish)
  - Ingredients: Under Image
  - Recipe: Under Ingredients
  - Tags: Under Recipe but above the 'Create' button

![cookbookcreate](cookbookcreate.png)

  - Post-Submission: Once created, it'll send users to their Posts and have a marker at the right that says 'Post Successfully Created'

![cookbookcreatesuccessful](cookbookcreatesuccessful.png)

  - If there was no post created, it will show an Error message.

![cookbookcreateerror](cookbookcreateerror.png)

**Create**

**Update:**

![cookbookupdateflow](cookbookupdateflow.png)

- Goal:
- This allows user to update the existing content and make necessary changes.
User Flow:
  - 1: 'Update' Button:
    - The user navigates to an existing post or a previously created recipe and there will be an 'Edit' option.
    - Clicking the button will open the existing content but now in modifiable mode so user can input changes then click 'Save' after.
  - 2: Decision Node:
    - Did they put the necessary changes? Were they valid?
    - Verification:
      - If yes, entity is updated with new data and will show user the verification popup "Changes saved!"
      - If no, error message will be triggered if there were no changes made and ask user to make changes. It will have a button to let users get out.
  - 3: Post-Update Navigation:
    - After, it will refresh page with newly inputted content in the post.

Wireframe:
- Layout:
  - In Posts (User's Posts), it'll have a 'Edit' button at the top-right.

![cookbookeditpost](cookbookeditpost.png)

  - Once clicked, the layout will be the already created post but modifiable and a 'UPDATE!' button at the bottom instead of 'Create!'

![cookbookeditupdate](cookbookeditupdate.png)

  - Post-Update: If successful, it'll show the user back to their Posts with a marker on the right that says the update was successful

![cookbookeditsuccessful](cookbookeditsuccessful.png)

  - If not, it'll give Error Message that tells them it's invalid and to go back.

![cookbookediterror](cookbookediterror.png)
