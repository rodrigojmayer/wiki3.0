## Deploying This Project

-> Clone repository
``` bash
git clone https://github.com/rodrigojmayer/wiki3.0.git
```

-> Create a Virtual environment using
``` bash

cd rodrigojmayer

mkvirtualenv --python=/usr/bin/python3.8 venv


```

-> Install all requirements using
``` bash

pip install -r requirements.txt


```

-> Add a new web app (select the last option to configure manually, no Django. And then the Python 3.8 version)

```
-> Setting up your Web app and WSGI file 

```
Source code: /home/rodrigojmayer/wiki3.0

Working directory: /home/rodrigojmayer

Virtual /home/rodrigojmayer/.virtualenvs/venv

# Paths
/static/    /home/rodrigojmayer/wiki3.0/encyclopedia/static

/media/	    /home/rodrigojmayer/wiki3.0/encyclopedia/static/media

```

Force HTTPS: ENABLE

```
-> WSGI
```
import os
import sys


path = os.path.expanduser('~/wiki3.0')

if path not in sys.path:
    sys.path.insert(0, path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'wiki.settings'

from django.core.wsgi import get_wsgi_application

from django.contrib.staticfiles.handlers import StaticFilesHandler
application = StaticFilesHandler(get_wsgi_application())

```