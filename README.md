# dckr_nginx-fpm
Base para inicio de aplicações com frontend e api php.

## Intruções
1 - Aplicaao frontend:
Mover a aplicação, se usa algum tipo de builder fazer o build antes, para o diretório src/front/

2- Aplicação API
Mover a API para o diretório src/api/
Caso o pondo de inicio da sua API não seja o diretório public, alterar o arquivo nginx/sites/api.conf para atender ao caminho correto.

* Checar no arquivo php-fpm/Dockerfile se as extenções PHP que sua API usa adicionar ao script as instruções para instalar as mesmas.

