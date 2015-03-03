    git clone https://github.com/webshootertk/ultraissue.git
    virtualenv env
    source env/bin/activate
    pip install -U -r requirements.txt
    vim issues/local_settings.py

Enter this

    import os
  
    SECRET_KEY = '<64bitkey>'

    STATICFILES_DIRS = (
        '/Path/to/static/',
    )

    MEDIA_ROOT = ''
    
    MEDIA_URL = ''
    
    STATIC_ROOT = ''
    
    STATIC_URL = '/static/'
    
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.sqlite3',
            'NAME': os.path.join(os.path.abspath("."), 'db.sqlite3'),
        }
    }

save

    python manage.py syncdb
    yes
    <admin>
    <email>
    <password>
    <password>
    python manage.py runserver
