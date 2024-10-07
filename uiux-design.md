
Search:
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

Update:
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
