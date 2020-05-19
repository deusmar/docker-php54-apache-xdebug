## Container c/ PHP 5.4 e xDebug (instalado via entrypoint.sh)
#### Disclaimer: Esse repositório foi criado apenas para ajudar um colega. Pode ser útil para o aprendizado sobre docker e entrypoints, php, apache, etc...

A ideia central era utilizar a imagem do PHP 5.4-apache e instalar o xDebug, descartando a alternativa de criação de Dockerfile. Com essa condição, foi feita a instalação do xDebug via entrypoint.

Para iniciar, execute o comando `docker-compose up -d`


#
## Docker + Windows + VS Code
Para utilizar no Windows 10 com VS Code é necessário instalar a extensão PHP Debug Adapter for Visual Studio Code:

## xdebug.ini
```
zend_extension=/usr/local/lib/php/extensions/no-debug-non-zts-20100525/xdebug.so
xdebug.default_enable=1
xdebug.remote_enable=1
xdebug.remote_handler=dbgp
xdebug.remote_port=9000
xdebug.remote_autostart=1
xdebug.remote_connect_back=1
xdebug.remote_log = /var/log/xdebug.log
```

## .vscode/launch.json
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Listen for XDebug",
            "type": "php",
            "request": "launch",
            "port": 9000,
            "pathMappings": {
                "/var/www/html": "${workspaceFolder}/"
            }
        }
    ]
}
```