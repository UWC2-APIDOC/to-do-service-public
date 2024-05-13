---
layout: page
---

# Tutorial: Update a user's name

In this tutorial, you will learn how to update a user's name.

## Prerequisites

Before starting, make sure you have completed and gone through the ["before you start a tutorial page"](docs/tutorials/before-you-start-a-tutorial.md)

## Update a user's name

1. Locate Git Configuration File

  * Global Configuration (for all repositories): Open ' ~/.gitconfig '.
  * Local Configuration (for a specific repository): Open ' .git/config within the repository directory '.

2. Edit Configuration File

  * Open the chosen configuration file in a text editor.

3. Update User's Name

  * Look for the [user] section.
  * Find the line ' name = Old Name '.
  * Replace Old Name with the new desired name, for example: ' name = New Name '.

4. Save Changes

  * Save the file and close the text editor.

5. Verify Changes

  * To check if the name has been updated, run: ' git config user.name '

6. Commit Changes

  * If you've edited the local repository's configuration file, commit the changes: ' git add .git/config ' and ' git commit -m "Update user name" ' after.

7. Push Changes

  * If you've committed changes and are working in a shared repository, push the changes: ' git push ' 


