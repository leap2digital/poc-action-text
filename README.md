# Action Text PoC

This is a Rails 6 + PostgreSQL app dockerized built to test Action Text.

It has a Post scaffolded model with a content attribute as rich text. You can create a new Post through the route /posts/new to see the Trix editor running.

You can attach files to the Trix editor and it will be processed by Active Storage locally. If you go to /posts/:id/ you can see the post's rich text content displayed.

# Set up

Before running the app you need to set up the containers:
```
docker-compose up
```

This should also build any container images you need. After that, you should open a new terminal window, attach to the web container and set up the database:
```
rails db:setup
```

Then you should be good to go.
