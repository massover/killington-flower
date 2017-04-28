# Celery Flower monitoring for killington

Requirements:

```
    python 3.6
    rabbitmq
```

## Local Development

```
    git clone https://github.com/massover/killington-flower.git
    pip install -r requirements-dev.txt
    honcho start
    open localhost:5555
```

Heroku:

Create an Heroku app:

    heroku create APP_NAME

Configure the app by providing your broker url (RabbitMQ, Redis, what have you) and a password for logging into Flower:

    heroku config:set BROKER_URL=redis://...
    heroku config:set FLOWER_BASIC_AUTH="username:password"

Push to heroku:

    git push heroku master

Now visit the app. It will ask for a username and a password which you defined above.
