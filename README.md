## Container c/ PHP 5.4 e xDebug (instalado via entrypoint.sh)
#### Disclaimer: Esse repositório foi criado apenas para ajudar um colega. Pode ser útil para o aprendizado sobre docker e entrypoints, php, apache, etc...

A ideia central era utilizar a imagem do PHP 5.4-apache e instalar o xDebug, descartando a alternativa de criação de Dockerfile. Com essa condição, foi feita a instalação do xDebug via entrypoint.

Para iniciar, execute o comando `docker-compose up -d`