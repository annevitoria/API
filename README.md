1. Clonando o repositório

A primeira coisa que eu fiz foi clonar o repositório do projeto LojaAPI.
Com isso, o código fonte do projeto ficou disponível na minha máquina local.


2. Subindo o container da API
Depois de clonar o projeto, eu usei Docker para subir a API. Certifiquei-me de que o Docker e o Docker Compose estavam instalados e, no diretório do projeto, rodei o comando abaixo:

*docker-compose up --build*


Esse comando construiu a imagem do container e iniciou o servidor. Assim que o processo terminou, a API ficou acessível em http://localhost:8000.
*

3. Fazendo testes com Postman
Agora vou explicar como fiz os testes utilizando o Postman.
3.1. Criando um produto
Para criar um produto, segui os seguintes passos no Postman:
Escolhi o método POST.
Usei a URL: http://localhost:8000/produtos/.
Content-Type: application/json
{ "nome": "Mouse", "preco": "3.00", "quantidade": 2, "categoria": 1}
Cliquei em Send.
Quando recebi o código de status 201 Created, soube que o produto foi criado com sucesso.

3.2. Filtrando um produto
Depois de criar o produto, eu quis confirmar se ele estava sendo listado corretamente. Para isso, fiz o seguinte:
Escolhi o método GET.
Usei a URL: http://localhost:8000/produtos/1/?format=json (substituindo 1 pelo ID do produto que criei).
Cliquei em Send.
{ "id": 1, "nome": "Mouse", "preco": "3.00", "quantidade": 2, "categoria": 1}

Com isso, confirmei que a API estava funcionando corretamente.



4. Referência de categorias
Ao criar produtos, usei os seguintes códigos de categorias como referência:

ID - Nome da Categoria

1. Acessórios de Informática

2. Memória RAM

3. Disco Rígido/SSD

4. Placa de Vídeo

5. Gabinete

6. Placa Mãe

7. Fonte

8. Processadores

9. Eletrodomésticos

10. Cama e Mesa
