# Heroku Deployment

### Intro:
Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications

heroku is


### depoly wiht heroku

1- Use the heroku login command to log in to the Heroku CLI:
```
heroku login
```
2- Start a new Git repository for your existing code base
```
$ cd /path/to/my/codebase
$ git init      (1)
$ git add .     (2)
$ git commit    (3)


```
2- Create an app on Heroku, which prepares Heroku to receive your source code. 
```
heroku create
```
3- deploy your code:
```
git push heroku main
```

4- Ensure that at least one instance of the app is running:
```
heroku ps:scale web=1
```

5- rename the created app
```
heroku apps:rename <anyName>
```

6- open the app!
```
heroku open
```

7- View information about your running app using one of the logging commands, `heroku logs --tail`