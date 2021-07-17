# Running Selenium with Chrome on Heroku
## Instructions

1. create an app on heroku
2. add 3 builpacks to heroko :  python, https://github.com/heroku/heroku-buildpack-google-chrome and
https://github.com/heroku/heroku-buildpack-chromedriver.
3. add these config vars to heroku, which will be the env variables for the deployment:
`
     CHROMEDRIVER_PATH = /app/.chromedriver/bin/chromedriver
     GOOGLE_CHROME_BIN = /app/.apt/usr/bin/google-chrome
`
4. make sure you're logged in to heroku on device
5. create project (ie. on pycharm) in env.
6. write your basic program + install packages you need
7. `pip3 freeze > Requirements.txt`
8. `echo > Procfile`
9. add this line to the procfile file:
    `web: python <name_of_file_to_run_on_startup.py>` (without the <> signs)
10. `git init`
11. `git add .`
12. `git commit -m "initial commit"`
13. `heroku git:remote -a <name of app on heroku>` (without <> signs)
14. `git push heroku master`
15. `heroku run python main` will run the main.py file and you'll see the output explained below. (optional)

Once app is deployed, whether or not you write line 15 (above), if you go to logs on heroku, you should see the page source contents of google.com printed out.


## Extras

For more info, the tutorial i've followed is "Running ChromeDriver with Python Selenium on Heroku",
by Andres Sevilla

link: https://www.youtube.com/watch?v=Ven-pqwk3ec

This repo has been created by myself, Given kibanza, along with the following readme file - to help anyone who needs
to use this.
