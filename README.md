# mysecureapi
# the urls as we expect them to appear

## these represent the routes

GET /api/posts to return all posts
GET /api/posts/:id provides the details of a posts
POST /api/posts creates a posts
PUT /api/posts/:id updates a posts
PATCH /api/posts/:id updates a posts
DELETE /api/posts/:id deletes a post


  
  post "posts" => 'posts#create'
  put "posts/:id" => 'posts#update'

  patch "posts/:id" => 'posts#update'
  delete "posts/:id" => 'posts#delete'
  get "me" => 'users#me'
  delete "me" => 'users#delete'
end







allow people to register to the site for post
POST /api/registrations

allow for admin login is handled by
doorkeeper, via
POST /oath/token
which will log a fellow in once that
fellow has a user name and and p-word

### the model

the models generation here were given per the assignment and
are created by rails generate model immediately after
the project creation rails new projectname

rails generate model User username:string password_digest:string
rails generate model Post title:string

note we still have not done a controller
