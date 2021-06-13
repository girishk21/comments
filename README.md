# Frontend Challenge

`docker-compose up`

## API Spec

- GET /posts

  - response

    - status {200}

      - PostsResponse {Object\<PostsResponse\>}

- GET /post/{post_id}

  - request

    - params

      - post_id {String}{Required}

  - response

    - status {200}

      - PostResponse {Object\<PostResponse\>}

- POST /post/like

  - request

    - body

      - post_id {String}{Required}

  - response

    - status {200}

    - status {400}

- POST /post/comment

  - request

    - body

      - post_id {String}{required}

      - comment_body {String}{required}

      - comment_id {String} parent comment_id for nested comments

  - response

    - status {200}

    - status {400}

Definition

- PostsResponse

  result {Array\<Post\>}

- PostResponse

  result {Object\<Post\>}

- Post

  id {String}

  body {String}

  title {String}

  likes {Number}

  comments {Array\<Comment\>}

  time_stamp {Number}

- Comment

  id {String}

  body {String}

  comments {Array\<Comment\>}

  time_stamp {Number}
