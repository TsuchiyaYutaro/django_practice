# django_practice
Django + Docker でアプリ開発環境を作成する

# SetUp

イメージのビルド

```
$ docker-compose build
```

アプリケーションの作成

```
$ docker-compose run web django-admin startproject <<application name>> .
```

権限の変更

```
$ chown -R $USER .
```

`./app/settings.py` の DATABASES の設定を下記に変更

``` python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'PASSWORD': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```

サーバを立てる

```
$ docker-compose up
```

http://localhost:8000
