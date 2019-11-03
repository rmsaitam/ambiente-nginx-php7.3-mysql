
Ambiente de desenvolvimento Docker com Nginx + PHP 7.3 e MySQL

**Pré-requisitos:** Ter o Docker e Docker-compose instalados.


[Instalando Docker no Windows 10](https://mundodacomputacaointegral.blogspot.com/2019/10/instalando-o-docker-no-windows.html)

[Instalando Docker e Docker-compose no Linux (qualquer distro)](https://mundodacomputacaointegral.blogspot.com/2019/10/instalando-docker-e-docker-compose-no-Linux.html)

Após ter instalado o Docker e Docker-compose, segue os procedimentos: 

1. Fork do repositório

2. Clonar o repositório forkado

3. Acessar o diretório onde salvou o clone do repositório

4. Execute `docker-compose up -d`

5. Adicione no arquivo hosts o app.local e app2.local

   **Windows:** _C:\Windows\System32\drivers\etc\hosts_

   **Linux:** _/etc/hosts_
   
6. Acessar o container PHP para instalar o Laravel Framework
   `docker exec -it app-php bash`
   
   Acessar _/var/www/html/app_ e execute `composer create-project --prefer-dist laravel/laravel .`
   
7. No browser acesse [http://app.local](http://app.local)

8. Esse ambiente de desenvolvido inclui 2 Vhosts no Nginx de exemplo para 2 projetos, mas pode ter N vhosts, basta reutilizar o arquivo _vhost.conf_ para o novo arquivo, alterando o _server_name_ e adicionar no _Dockerfile_ do PHP. Lembrar de adicionar no arquivo hosts para cada Vhost do projeto.

Feito!


