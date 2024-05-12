# Tutorial: Searching for users
You can search for users by first name, last name, full name, email, or user ID. The To-Do service returns only results that match the search parameters exactly.  **Note:** User names and emails are case sensitive.



# Request format
To search for a specific user, append a question mark (`?`) to `/users` in the URL, followed by the relevant query parameters.
* To search by a specific first name, add the `first_name` parameter to the URL followed by an equals sign (`=`) and the desired first name.
* To search by a specific last name, add the `last_name` parameter to the URL followed by an equals sign (`=`) and the desired last name.
* To search by both first and last names, append `first_name=` followed by the first name, and `&last_name=` followed by the last name to the URL.
* To search by a specific email, add the `email` parameter to the URL followed by an equals sign (`=`) and the desired email address.
* To search by user ID, add the `id` parameter to the URL followed by an equals sign (`=`) and the desired user ID.

# Response format
The service returns all associated user info that matches your criteria. If more than one user matches your search term, the service will return multiple users. 

If no user matches the search criteria, the service will return an empty array ([]).

# Tutorial topics
For in-depth tutorials with examples, see the following topics:
* [Tutorial: Get a user by name](get-a-user-by-name.md)
* [Tutorial: Get a user by email address]() 
[comment:] get user by email address is david's topic 