# TESTE DOM-PIXEL
Sistema de Catálogo de Produtos
Uma aplicação simples de gerenciamento de produtos para a seleção de Desenvolvedor PHP.

## Como executar o projeto

### Clone o repositório
git clone https://github.com/VictorMGomes/teste-dom-pixel.git

### Entre na pasta do projeto
cd teste-dom-pixel

### Copie o arquivo .env.example e renomei para .env e altere as variais que deseja
cp .env.example .env

### Instale os pacotes
docker run --rm --interactive --tty --volume $PWD:/app --user $(id -u):$(id -g) composer install

### Execute o projeto
./vendor/bin/sail up -d

### Gere a chave da aplicação
./vendor/bin/sail artisan key:generate

### Execute as migrations
./vendor/bin/sail artisan migrate
