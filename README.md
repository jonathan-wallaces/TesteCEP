# API ENDEREÇOS
API desenvolvida para realizar cadastro, edição, deleção e atualização de endereços. A API consome os dados retornados do webservice ViaCEP. O cadastro dos endereços são realizado à partir do cep informado.
O projeto foi desenvolvido utilizando os conceitos de Clean Arch.

-Java 17
-Spring Boot
-Lombok
-Banco de Dados MySQL

# API ENDEREÇOS
http://localhost:8080/ - API Endereços que disponibiliza todas as funcionalidades.
Há um arquivo dat.sql que insere alguns dados no banco.

# DOCUMENTAÇÃO
- http://localhost:8080/
- EndPoints
    - POST http://localhost:8080/endereco/{cep} - Procura o cep informado na API VIACEP e com o JSON retornado salva os dados solicitados no banco e envia um e-mail automaticamente.
    - GET http://localhost:8080/endereco - Lista todos os endereços cadastrados no banco de dados
    - PUT http://localhost:8080/endereco - Edita um endereço específico. Um exemplo de Json esperado no corpo da requisição:
        -   {
	            "id": Long,
	             "logradouro": "rua a",
	             "complemento": "apartamento 1",
	             "bairro": "centro",
               	"localidade":"bahia",
	               "uf":"bh"
               }
               
    - DELETE http://localhost:8080/endereco/{id} - Deleta um endereço cadastrado 

