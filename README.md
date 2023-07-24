# TESTE DOM-PIXEL
## Sistema de Catálogo de Produtos
Uma aplicação simples de gerenciamento de produtos para a seleção de Desenvolvedor PHP.

## Como executar o projeto

### Requisitos
#### Docker e Docker Composer
Este projeto é executado via containers: https://docs.docker.com/
Obs: Mas também pode ser utilizado sem dockerização, sendo necessária a instalação dos serviços de forma manual.
    Verificar o composer.json.
#### Recomendado o uso de Linux ou WSL
Para as instruções de comando, outras plataformas talvez necessitem de adaptações.
#### Laravel Sail
Este projeto é executado utilizando Laravel Sail: https://laravel.com/docs/10.x/sail

### Instruções
#### Clone o repositório
`git clone https://github.com/VictorMGomes/teste-dom-pixel.git`
#### Entre na pasta do projeto
`cd teste-dom-pixel`
#### Copie o arquivo .env.example e renomei para .env e altere as variais que deseja
`cp .env.example .env`
#### Instale os pacotes
`sudo docker run --rm --interactive --tty --volume $PWD:/app --user $(id -u):$(id -g) composer install`
#### Execute o projeto
`sudo ./vendor/bin/sail up -d`
#### Correção de permissões, necessário em alguns ambientes
`chmod -R 777 storage && chmod -R 766 .env`
#### Gere a chave da aplicação
`sudo ./vendor/bin/sail artisan key:generate`
#### Execute as migrations
`sudo ./vendor/bin/sail artisan migrate`
