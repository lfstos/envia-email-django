# envia-email-django
Envia email com Django

Fontes: <br> <br>

https://docs.djangoproject.com/en/3.1/topics/email/ <br><br>
https://marcelogomesrp.blogspot.com/2014/05/envio-de-email-com-django-pelo-console.html <br> <br>
https://desenvolvo.wordpress.com/2014/02/22/envio-de-email-com-django-pelo-console/ 

````
Para rodar o projeto precisamos configurar as seguintes variáves no settings.py

EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
DEFAULT_FROM_EMAIL = '#####'
EMAIL_USE_TLS = True
EMAIL_HOST = '#######'
EMAIL_HOST_USER = '########'
EMAIL_HOST_PASSWORD = '########'
EMAIL_PORT = ###

No terminal precisamos acessar o python console
python manager.py shell

Depois fazemos o seguinte import e em seguida rodamos o seguinte código.

from django.core.mail import send_mail

send_mail(
    'Teste', 
    'Teste de envio de email com Django', 
    'fulano@gmail.com', 
    ['beltrano@gmail.com']
)
