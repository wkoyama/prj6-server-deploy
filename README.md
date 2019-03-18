# Configuração de servidor Linux - Udacity

Esse projeto está alocado na [Amazon Lightsail](https://lightsail.aws.amazon.com) para a conclusão do curso.

Com a chave privada enviada, colocar na pasta ~/.ssh.
O servidor pode ser acessado através do seguinte comando e logo após inserir a passphrase da key:

    ssh grader@34.205.81.139 -p 2200 -i .ssh/UdacityCourse


A URL para acessar a aplicação funcionando é a seguinte:

    http://www.34.205.81.139.xip.io
    

## Resumo da aplicação

Neste projeto para a unidade de configuração de servidor Linux, subimos uma das aplicações desenvolvidas no curso ("Catálogo de Itens")

Alterei, a principio, a aplicação para funcionar com o [PostgreSQL](https://www.postgresql.org/) antes não usado. 

A aplicação para facilitar um pouco na subida para produção fiz uso do ambiente virtual com [venv e virtualenv](https://packaging.python.org/guides/installing-using-pip-and-virtualenv/).

Já na configuração do servidor foi necessário usar alguns softwares descritos na seção ["Recursos Usados"](#recursos-usados) e modificá-los para o funcionamento, sendo alguns descritos abaixo:
  
  - Instalação do Redis
  - Configuração do SSH
  - Configuração do Firewall
  - Configuração do NTP
  - Instalação do Apache2
  - Instalação e configuração do Postgresql
  - Configuração do WSGI e Apache
  
## [Recursos Usados](#recursos-usados)

  * [Redis](https://redis.io/)
  * [PostgreSQL](https://www.postgresql.org/)
  * [UFW](http://wiki.ubuntu-br.org/UFW)
  * [Apache2](http://httpd.apache.org/)
  * [WSGI](https://modwsgi.readthedocs.io)
  * [Venv e Virtualenv](https://packaging.python.org/guides/installing-using-pip-and-virtualenv/)
  * [xip.io](http://xip.io/)
  * [Amazon Lightsail](https://lightsail.aws.amazon.com)
  * [Google OAuth2](https://developers.google.com/identity/protocols/OAuth2)
  
## Notas de desafios superados

  - O desafio de adaptar o projeto e servidor com a mesma versão linux e adaptação de bibliotecas para funcionar bem com a versão 3.7 do Python, [este link](https://medium.com/@garethjohnson_52722/serve-python-3-7-with-mod-wsgi-on-ubuntu-16-d9c7ab79e03a) me ajudou com isso.
  - O uso do mod_wsgi com a versão do Python 3.7. Além da mudança das configurações para atender o projeto com autenticação.
  - A criação dos usuários e permissões do Postgresql e uso do driver psycopg2 que foi onde me deparei com a maior parte dos conflitos com a versão 3.7
  
