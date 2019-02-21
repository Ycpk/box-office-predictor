## Instructions

### Dependancies:

Install all dependencies needed by the application.

1.  Go to root of directory and using terminal/cmd run command

```python
pip install -r requirements.txt
```

2. Depending on the network, it may take some time to download all
   dependencies.

### API account creations:

At first we need to create online accounts needed to grab the data from various
sources.

1. [Youtube Data API](https://developers.google.com/youtube/v3/getting-started) (Free)
2. [Twitter API](https://twitter.com/login?redirect_after_login=https%3A%2F%2Fdeveloper.twitter.com%2Fen%2Fapply) (Free)
3. [TheMovieDB API](https://developers.themoviedb.org/3/getting-started/introduction) (Free)
4. [Opencage API](https://opencagedata.com/api) (Free)

### API Keys Configurations:

1. Youtube Data API
   a. Follow instructions from "Youtube API Credentials" section (located near end of document) and create OAuth credentials.
   b. These are not needed to be copied in config.py file as they reside in separate file.
2. Twitter API
   After signing up locate and copy the credentials consumer key, consumer
   secret,access token key,access token secret into appropriate placeholders in config.py
3. MovieDB API key
   Paste the api key in placeholder of config.py
4. Opencage API key
   Paste the api key in placeholder of config.py

### Starting the Webapp

1. After all above steps are completed, open terminal/cmd in root folder of the app.
2. run command

```shell
python app.py
```

3. While running the app for the first time, google OAuth flow needs to be
   completed. A google sign in page will open where you should sign in with google account from which
   the project is created. A page with message ‘Authentication flow completed’ will be shown.
4. This is one time activity as long as newly generated Oauth credentials are stored
   on the system
5. In the browser address bar enter localhost:5000, and app’s home page will
   appear.
6. For any subsequent web app usages, just use command python app.py in root
   directory.
7. Make sure the app is not already running before starting it. If it is, you will need to
   manually kill that process using commands like:

```shell
ps -ef | grep python
```

locate pid of app.py process and then use following command

```shell
kill -SIGKILL pid
```

### Softwares

Any IDE such as VS Studio code will make running the app a pleasing experience.

### Youtube API Credentials

Creating Oauth Credentials for Youtube API

1. After creating google console project, go to project dashboard.
2. From the left bar , select API credentials
3. Click on Create credentials -> Oauth Client ID
4. Select Application type as web application
5. In the “Authorized Javascript Origins” list under Restrictions section, add following URLs
   separately : http://localhost:8888 , http://localhost:8080
6. Add above two urls under “Authorized Redirect URIs” too
7. Click on create.
8. Press Ok on OAuth Client screen
9. You will now see your credentials generated under OAuth 2.0 client IDs of credentials page.
10. Click on credential and download json
11. Copy the json to Project root directory (on the same level as app.py) and rename it to
    client_secrets.json
12. Now go to OAuth consent screen tab
13. Enter name of application as Box Office Prediction, enter email and save it.

## User Interface

Once user enter a movie name in the search box of the home page, results are presented as follows
![alt text][logo]
[logo]: https://github.com/Ycpk/box-office-predictor/blob/master/screenshot.png "Box Office Predictor"
