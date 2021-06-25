# Post Place

Post Place is a social media application where users can make posts and interact with posts by liking and commenting on them.

## How to run the app

1. Fork or clone the github repo and open up the folder in the CLI
2. Install all dependencies (Bring up 2 terminals, cd into client on one and server on the other, run npm i in both.)
3. Hook up an empty MongoDB collection to the server and set a JWT secret, setting them to CONNECTION_URL and JWT_SECRET in an .env file in the server folder.
4. Connect your server to the clientside via .env files in client / server folders.
- Optionally connect a google OAuth clientID to the front end if it isn't too much trouble and/or you want the google login to work.
5. Run the client and server locally via the npm start command.
6. Navigate to the URL you chose for the clientside and the app should be running.

## Features

1. a user can sign up for an account, sign in, sign in via google, or use a guest account.
2. A signed-in user can make, edit, delete, or like posts.
3. A signed-in user can make, delete or like comments tied to a specific post by visiting its page.
4. All actions where applicable will be displayed in real time to all users.
5. Actions are saved to a database so data is persistent across visits.
6. The site has different views dependent on window size and looks normal / functions properly down to 250px width.

### How to interact with posts

1. Click the sign in button at the top-right and sign up, sign in, or use a guest account. You can now interact with others' posts and comments.
2. The like button is in the bottom left corner of posts. You can click it again to unlike after you've liked a post.

### Making a post

1. Once signed in, fill out the title, message fields and optionally the tag and image fields. Press enter to add tags.
2. Submit and your post will appear for all users in real time, signed in or not.

### Updating and deleting your post

1. If you made a post, a small 3 dot icon (...) will be seen in the top right of the post on the home page. Click it.
2. Adjust the form values and press submit as you did when you first created it.
3. If you'd like to delete your post, a small delete button will be seen in the bottom right of the post.
4. If you press this button, your post will be permanently deleted.

### Making, deleting, and liking comments
1. Click on a post to be directed to its page.
2. Type out a comment in the text field below the picture and other information about the post.
3. Click submit.
4. Liking and deleting work similarly to posts. Click the thumb to like/unlike, click the delete button if you want to delete your comment.

## Future features
- Proper XSS protection. (If you visit the live version please don't blow my site up.)
- Other social media actions like sharing/reposting others' posts.
- A user profile page where one can see all the posts a specific user has made and maybe their comments on other posts.
- Proper account recovery stuff and email validation.

## Dependencies
- React
- Node
- Express
- MongoDB / mongoose
- moment
- axios
- material-ui core/lab/icons
- redux toolkit
- react-router-dom
- socket.io / socket.io-client
- jwt / jwt-decode
- react-file-base64
- react-google-login
- cors
- bcrypt
- dotenv