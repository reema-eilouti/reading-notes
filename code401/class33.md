# Read : 33

## Authentication & Production Server

- The token authentication works by exchanging username and password for a token that will be used in all subsequent requests so to identify the user on the server side.

- JWT stand for JSON Web Token and it is an authentication strategy used by client/server applications where the client is a Web application using JavaScript and some frontend framework like Angular, React or VueJS.

- **Implementing the Token Authentication**:

    - We need to add two pieces of information in our `settings.py` module. 
    - First include `rest_framework.authtoken` to your `INSTALLED_APPS` and include the `TokenAuthentication` to `REST_FRAMEWORK`.

```
INSTALLED_APPS = [
    # Django Apps
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    # Third-Party Apps
    'rest_framework',
    'rest_framework.authtoken',  # <-- Here
    # Local Apps (Your project's apps)
    'myapi.core',
]
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework.authentication.TokenAuthentication',  # <-- And here
    ],
}
```

- Then we migrate. After creating a user and trying to use it it'll block you.

- To know what token you have use:
```
python manage.py drf_create_token vitor
```

- But if you use the token, then it'll work. For example:
```
http http://127.0.0.1:8000/hello/ 'Authorization: Token 9054f7aa9305e012b3c2300408c3dfdf390fcddf'
```

- It is important to note that the default Token implementation has some limitations such as only one token per user, no built-in way to set an expiry date to the token.

- Adding this to code not into the url field will look like this:
```
import requests
url = 'http://127.0.0.1:8000/hello/'
headers = {'Authorization': 'Token 9054f7aa9305e012b3c2300408c3dfdf390fcddf'}
r = requests.get(url, headers=headers)
```

##### [Go Back](code_401_reading_notes.md)