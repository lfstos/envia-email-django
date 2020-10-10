# envia-email-django
Envia email com Django

````
Precisamos instalar o django no ambiente virtual
- pip install django

Para rodar o projeto precisamos configurar as seguintes variáves no settings.py

- EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
- DEFAULT_FROM_EMAIL = '#####'
- EMAIL_USE_TLS = True
- EMAIL_HOST = '#######'
- EMAIL_HOST_USER = '########'
- EMAIL_HOST_PASSWORD = '########'
- EMAIL_PORT = ###

Se for rodar pelo pelo navegador, precisamos rodar o servidor django e depois chamar o endereço:
- localhost:8000/envia-email

Se for rodar pelo console do Python
- python manager.py shell

Depois fazemos o seguinte import e em seguida rodamos o seguinte código.

from django.core.mail import send_mail

send_mail(
    'Teste', 
    'Teste de envio de email com Django', 
    'fulano@gmail.com', 
    ['beltrano@gmail.com']
)
