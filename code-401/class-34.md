# Configuring Django Settings: Best Practices

### django-environ

Environment variables are the perfect place to store settings.
This app gives a well-functioning API for reading values from environment variables or text files, handful type conversion.

### 12 Factors

12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud.
It was created by Heroku, a well-known Cloud hosting provider.

**An example `setting.py` using django-environ:**

```python
import environ


root = environ.Path(__file__) - 3  # get root of the project
env = environ.Env()
environ.Env.read_env()  # reading .env file

SITE_ROOT = root()

DEBUG = env.bool('DEBUG', default=False)
TEMPLATE_DEBUG = DEBUG

DATABASES = {'default': env.db('DATABASE_URL')}

public_root = root.path('public/')
MEDIA_ROOT = public_root('media')
MEDIA_URL = env.str('MEDIA_URL', default='media/')
STATIC_ROOT = public_root('static')
STATIC_URL = env.str('STATIC_URL', default='static/')

SECRET_KEY = env.str('SECRET_KEY')

CACHES = {'default': env.cache('REDIS_CACHE_URL')}
```

### Django Settings: Best practices

- Keep settings in environment variables.
- Write default values for production configuration (excluding secret keys and tokens).
- Don’t hardcode sensitive settings, and don’t put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.

# How Does SSH Work
SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet.

There are three different encryption technologies used by SSH:

- Symmetrical encryption
- Asymmetrical encryption
- Hashing.

### Symmetric Encryption

Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the 
client and the host. Effectively, any one possessing the key can decrypt the message being transferred.

### Asymmetric Encryption
uses two separate keys for encryption and decryption. These two keys are known 
as the public key and the private key. Together, both these keys form a public-private key pair.

### Hashing
One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted.
This means that if a client holds the correct input, they can
generate the crypto-graphic hash and compare its value to verify whether they possess the correct input.

    
   
