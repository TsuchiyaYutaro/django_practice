# django_practice
Django の練習

# SetUp

イメージのビルド

```
$ docker-compose build
```

プロジェクトの作成

```
$ docker-compose run web django-admin startproject <<project name>> .
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
