-Create a virtual environment
- Activate virtual environment
- Install requirements using 'pip install -r requirements.txt'

-Start your project
- cd into project you have created and then,
- create apps

-Configure your project
- Go to settings.py and add the apps that you have created
 
 # Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    
    # Created apps
    'patients',
    'doctors',
    'appointments',
    'billing',
    
    # Requirements
    'rest-framework',
    'corsheaders',
    'drf_yasg',
    'django_filters',
]

# Configure Rest Framework

REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework.authentication.TokenAuthentication',
    ],
    
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permission.IsAuthenticated',
    ],
    
    'DEFAULT_FILTER_BACKENDS': [
        'django_filters.rest_framework.DjangoFilterBackend',
        'rest_framework.filters.SearchFilter',
        'rest_framework.filters.OrderingFilter',
    ],
}
 