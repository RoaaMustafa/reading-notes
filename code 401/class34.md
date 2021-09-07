# API Deployment

## Django Settings Best Practices

### Managing Django Settings: Issues

+ Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. 
+ Sensitive data. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. 
+ Sharing settings between team members. You need a general approach to eliminate human error when working with the settings. 
+ Django settings are a Python code. This is a curse and a blessing at the same time. 


### Setting Configuration: Different Approaches

+ settings_local.py
    + settings.py file:
```

ALLOWED_HOSTS = ['example.com']
DEBUG = False
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'production_db',
        'USER': 'user',
        'PASSWORD': 'password',
        'HOST': 'db.example.com',
        'PORT': '5432',
        'OPTIONS': {
            'sslmode': 'require'
        }
    }
}

...

from .settings_local import *

```

    + settings_local.py file:
	
```
ALLOWED_HOSTS = ['localhost']
DEBUG = True
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'local_db',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}
	
```
+ Pros:  Secrets not in VCS.
        
     + Cons:
         + settings_local.py is not in VCS, so you can lose some of your Django environment settings.
         + The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
         + You need to have settings_local.example (in VCS) to share the default configurations for developers.

### Separate settings file for each environment

```

from .base import *


ALLOWED_HOSTS = ['localhost']
DEBUG = True
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'local_db',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}


```


To run a project with a specific configuration, you need to set an additional parameter:

`python manage.py runserver --settings=settings.local`


+ Pros:
All environments are in VCS.

It’s easy to share settings between developers.


+ Cons:
+ 
You need to find a way to handle secret passwords and tokens.

“Inheritance” of settings can be hard to trace and maintain.


### Django Settings: Best practices

+ Keep settings in environment variables.
+ Write default values for production configuration (excluding secret keys and tokens).
+ Don’t hardcode sensitive settings, and don’t put them in VCS.
+ Split settings into groups: Django, third-party, project.
+ Follow naming conventions for custom (project) settings.




## SSH Tutorial

### How Does SSH Work

The SSH command consists of 3 distinct parts:

`ssh {user}@{host}`


### Understanding Different Encryption Techniques

There are three different encryption technologies used by SSH:

+ Symmetrical encryption

![symmetric-encryption](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/symmetric-encryption-ssh-tutorial.jpg)

+ Asymmetrical encryption

![asymmetric-encryption](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/asymmetric-encryption.jpg)


+ Hashing.


![ssh-tutorial-hash](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/ssh-tutorial-hash.jpg)

### How Does SSH Work with These Encryption Techniques


SSH operates on TCP port 22 by default (though this can be changed if needed).

The host (server) listens on port 22 (or any other SSH assigned port) for incoming connections. 

It organizes the secure connection by authenticating the client and opening the correct shell environment if the verification is successful.

![ssh-client-and-server.](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/ssh-client-and-server.jpg)

#### Here is how the algorithm works at a very basic level:

+ Both the client and the server agree on a very large prime number, which of course does not have any factor in common. This prime number value is also known as the seed value.
+ Next, the two parties agree on a common encryption mechanism to generate another set of values by manipulating the seed values in a specific algorithmic manner. These mechanisms, also known as encryption generators, perform large operations on the seed. An example of such a generator is AES (Advanced Encryption Standard).
+ Both the parties independently generate another prime number. This is used as a secret private key for the interaction.
+ This newly generated private key, with the shared number and encryption algorithm (e.g. AES), is used to compute a public key which is distributed to the other computer.
+ The parties then use their personal private key, the other machine’s shared public key and the original prime number to create a final shared key. This key is independently computed by both computers but will create the same encryption key on both sides.
+ Now that both sides have a shared key, they can symmetrically encrypt the entire SSH session. The same key can be used to encrypt and decrypt messages (read: section on symmetrical encryption).

### Authenticating the User
The final stage before the user is granted access to the server is authenticating his/her credentials. For this, most SSH users use a password. The user is asked to enter the username, followed by the password. These credentials securely pass through the symmetrically encrypted tunnel, so there is no chance of them being captured by a third party.

Although passwords are encrypted, it is still not recommended to use passwords for secure connections. This is because many bots can simply brute force easy or default passwords and gain access to your account. Instead, the recommended alternative is SSH Key Pairs.
