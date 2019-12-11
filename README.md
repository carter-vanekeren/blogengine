# BlogEngine
Project Type: C

Group Members Name(s): Carter Van Ekeren

[Live Application Link](https://flask-blogengine.herokuapp.com)

[Github Repository](https://github.com/carter-vanekeren/blogengine)

### Technologies used
- Flask Framework (Python)
- Bootstrap Framework (CSS)
- HTML
- [Other Dependencies](https://github.com/carter-vanekeren/blogengine/blob/master/requirements.txt)
- API's
  - Gravatar
- Heroku (Deployment)
- VSCode (Editor)


### Controllers
- Index
  - Handles the creation of posts and the display of posts from the current user and users that the current user follows.
- Login
  - Handles user authentication
- Logout
  - Logs user out of application 
- Register
  - Handles creation of new user account
- User
  - Handles User profile page.  Displays avatar, username, about me section, last see online, follower/following count, follow/unfollow links and shows all posts that user has made.
- Edit profile
  - Handles user changing username and about me section
- Follow
  - Allows user to follow other users
- Unfollow
  - Allows users to unfollow other users
- Explore
  - Shows posts from all registered users.  

### Views
- Base 
  - All views inherit from this view.
  - Contains navigation and flash messages
- Index
  - Used for home page and explore page.
  - Lists posts, deals with pagination and allows user to create posts if on the Home page
- Error
  - Defines views for:
    - 404 
    - 500
- Login
  - Displays login form and a link to register
- Register
  - Displays registration form
- User
  - Displays user profile page, summary section and a posts listing section
- Post
  - Handles view of a post object

### Tables 
- User
  - Table that represents a user
  - Attributes
     - id (Primary key)
     - username
     - email
     - password_hash
     - about_me
     - last_seen
- Post
  - Table that represents a post, has a relationship with user
  - Attributes
    - id
    - body
    - timestamp
    - user_id (Foreign key)
- Followers   
  - Table that represents followers, self-referential relationship with user
  - Attributes
    - follower_id (Foreign key)
    - followed_id (Foreign key)
