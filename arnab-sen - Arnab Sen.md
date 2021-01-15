# Developer - Winter of Code 2020

# Arnab Sen
### DSC-X : OMG-Frames

## About Me

I am [Arnab Sen](https://www.linkedin.com/in/arnab-sen-b6950a194/), a Computer Science undergraduate student of [IIEST, Shibpur](https://www.iiests.ac.in/).

The project was under the mentorship of [Anubhav Singh](https://github.com/xprilion)

## Overview
Since there was no repo for the backend, I worked on a separate repo from scratch

Repo link: https://github.com/dsc-x/omg-frames-api
- Commits: [29](https://github.com/dsc-x/omg-frames-api/commits?author=arnabsen1729)
- Pull Requests: [4](https://github.com/dsc-x/omg-frames-api/pulls?q=is%3Apr+author%3Aarnabsen1729)
- [`2799++ 413--`](https://github.com/dsc-x/omg-frames-api/graphs/contributors)


## Contributions

### 1. User registration and Login. 

**Commit:** [b82a098](https://github.com/dsc-x/omg-frames-api/commit/b82a098217c54566de5f5cd2ea54bf260b69a9cf)

Implemented the APIs for user registration and user login. The database used for storing the data of the user is Firebase Realtime Database. The reasons for choosing Firebase was:
- It was was to setup.
- Almost zero-configuration required, only the API keys needed to be changed.

At first, I thought of implementing Google Oauth, but later my mentor Anubhav asked me to set up our own user authentication and use JWT tokens(using the `jwt` library of python). So all the user data is stored in the database (password is hashed using `pbkdf2_sha256` before it is stored).

Registering the user:

![Imgur](https://raw.githubusercontent.com/arnabsen1729/static-content/master/woc2020/register.gif)

Logging in as the user:

![Imgur](https://raw.githubusercontent.com/arnabsen1729/static-content/master/woc2020/login.gif)

### 2. CRUD operations on the frames of user

**Commits:** [0d4de73](https://github.com/dsc-x/omg-frames-api/commit/0d4de73d19ec50b3c97b70ca5b665501bcb21aa3), [135fb64](https://github.com/dsc-x/omg-frames-api/commit/135fb64b490c69b2955442b152ec46880fe35ac5), [e8253df](https://github.com/dsc-x/omg-frames-api/commit/e8253df2a06ccf1a3de8ea9b1c767a15b069f704)

Every user has a frames array, when the user uploads the frame, it gets saved in the array. So, the APIs implemented are:
- Saving new frames `POST` 
- All the user frames `GET`
- Updating an existing frame `PUT`
- Deleting a frame `DELETE`

Also, every route related to the frame is protected with a JWT token. The token is encoded in a way that it has the `user_id` of the user as a payload and is signed with a secret key. So when the token is sent in the Authorization header along with the request, it is first verified with the secret key and then the payload is extracted and all the necessary DB operation is done after that. 

### 3. Email Service added

**PR:** [#15](https://github.com/dsc-x/omg-frames-api/pull/15)

For the forget password we needed to setup an Email Service. This was a rough sketch that I made to implement the idea:

![Imgur](https://raw.githubusercontent.com/arnabsen1729/static-content/master/woc2020/email.png)

Briefly, there will be a URL sent to the user which will have a token. This token was generated using the `itsdangerous.serializer` which had an expiry of 24 hours. On clicking that URL the user will be redirected to a new reset password form, which will send a request to another endpoint to update the password. So for this I had to implement two APIs:
- POST  /send-reset-mail
- POST  /update-password

Also, when the user registers there is a mail sent to the user with a successful registration message. It is implemented in commit [e632b57](https://github.com/dsc-x/omg-frames-api/commit/e632b575940cd3b00542f13629935fb2943ee01c).

The templates of the email are responsive.

Welcome Mail format

![Imgur](https://raw.githubusercontent.com/arnabsen1729/static-content/master/woc2020/welcome_mail.png)

Reset Mail format

![Imgur](https://raw.githubusercontent.com/arnabsen1729/static-content/master/woc2020/reset_mail.png)


### 4. API documentation using Swagger

**Commits:** [79ecbdc](https://github.com/dsc-x/omg-frames-api/commit/79ecbdcfa0eaf881e774dac1b32e2a8b3b2c425a), [1fd7bbe](https://github.com/dsc-x/omg-frames-api/commit/1fd7bbe241d2124d21add990574fb53464f3620a), [7f9fd98](https://github.com/dsc-x/omg-frames-api/commit/7f9fd9872edbf44b2749de6f4c91fd451b03364a)

For the ease of testing for the frontend developers and for future contributors, API documentation is very helpful. Anubhav sir suggested me to use Swagger. Swagger is very easy to use, has a simple dashboard, shows the object models, and is widely popular. For every API that is implemented in the server, I have added the routes to swagger so that routes can be tested from the dashboard itself. All the related document files are stored in `.yml` format in the [`docs`](https://github.com/dsc-x/omg-frames-api/tree/master/docs). 

The apidocs is deployed at: [https://api.iwasat.events/apidocs/](https://api.iwasat.events/apidocs/)

![Imgur](https://raw.githubusercontent.com/arnabsen1729/static-content/master/woc2020/swagger.gif)

### 5. Deployed the backend in a VPS

For the deploying the backend on the server:
- Created deploy keys for the repo.
- Created a new gunicorn service `/etc/systemd/system/omg-frames-api.service`.
- Configured NGINX reverse proxy to map the address `api.iwasat.events` to the service running at a particular port i.e. the flask application.
- Secured the application with SSL encryption using Let's Encrypt.

Also implemented a CI/CD pipeline to automate the build and deploy process. **Commit:** [95224b97](https://github.com/dsc-x/omg-frames-api/commit/95224b97a74cc5ab7de6e9bdb3f4fe514d31bedd). So any changes pushed to master will trigger an action [https://github.com/dsc-x/omg-frames-api/actions](https://github.com/dsc-x/omg-frames-api/actions) which will:
1. Pull all the latest changes in the server
2. Install any necessary package from requirements.txt
3. Reload the daemon and restart the gunicorn service.

<hr>

For every commit I made sure
- The Python files followed the Python Flake8 linting conventions. 
- Neccesarry comments and [Google styled docstrings](https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html) for code redability. **Commit:** [74ce484](https://github.com/dsc-x/omg-frames-api/commit/74ce48426cc6c70fef0b2aae1a487e131dcb37e2)

I further added a Dockerfile and a Makefile for the ease of deployment and development. **Commit:** [6e0f81a](https://github.com/dsc-x/omg-frames-api/commit/6e0f81a2d9e6189d617a85635887c80943f7839f)

## Further Scope

I think there is a further scope to improve the performance of the APIs. 
1. If a particular User has more than one frame, sending one single GET request with all the images becomes very time-consuming. So Anubhav sir suggested that we could have rather used two different endpoints one with a query and the other without. So a GET request to `/frames` will respond with all the ids of the frame ( not the data ), but the GET request to `/frame?id=` will respond with the frame_data of frame whose id is provided in query. This will improve the performance considerably, also the user doesn't have to wait for all the images to load. 

    **Issue:** [#17](https://github.com/dsc-x/omg-frames-api/issues/17)

2. When a user registers we are not checking the fact if the email they provided was actually theirs, so for that we can implement a mail verification service. There can be different approaches, one would be to send a secret link, and visiting that link will confirm it's their email. Other, would be to use a secret code which they have to enter to verify. Both the methods has its pros and cons. 

    **Issue:** [#16](https://github.com/dsc-x/omg-frames-api/issues/16)

3. Using some compression before storing the images in the database. Since we are using base64 encoding for the image, the length increases by approximately 30-35% but using some kind of compression, like `gzip` can reduce the inflation to `2-10%`. This can be a minor improvement in fetching the data from the Firebase database. I have also written a [script](https://gist.github.com/arnabsen1729/833df5001e14206d0340925bdd731708) that can demostrate the compression percentage.

    **Issue:** [#18](https://github.com/dsc-x/omg-frames-api/issues/18)

## Overall Experience

I am really thankful to the Winter of Code for giving me this amazing opportunity to work on a nice project under DSC-X. Also, glad to be mentored by [Anubhav Singh](https://github.com/xprilion). I learned a lot throughout the entire process, not just about the project but also about the practices of Open Source. I believe this experience of WoC will definitely help me in my GSoC.  I also express my gratitude to [Awantika Nigam](https://www.linkedin.com/in/awantika-nigam-2181861a8/) and [Rajinderpal Singh](https://www.linkedin.com/in/rajinderpal-singh-580445190/) for being so collaborative.
