# CRUD Python com Flask, SQLAlchemy e Front-end Angular
Este é um projeto simples de CRUD (Create, Read, Update, Delete) em Python utilizando o framework Flask e o ORM SQLAlchemy. O projeto gerencia informações sobre veículos, como nome, marca, modelo, foto, valor e quilometragem.
O projeto inclui um frontend desenvolvido em Angular na versão 16.2.0. Este frontend consome os endpoints fornecidos pelo backend Python.

# Pendências
- Implementar autenticação nas requisições.
- Campo para subir fotos do veículo a ser cadastrado (No projeto o campo foto está como uma string).
- Admin só pode ser acessado se o usuário fizer autenticação.

# Requisitos
- Python 3.x
- Flask
- Flask-SQLAlchemy
- Flask-CORS
- PostgreSQL
- Angular

# Configuração do Banco de Dados
- O aplicativo está configurado para utilizar um banco de dados PostgreSQL.
- Certifique-se de ter o PostgreSQL instalado e criar um banco de dados chamado "cadastro-veiculos".
  - app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql://postgres:suasenha@localhost/cadastro-veiculos'
  - app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False


# Estrutura do Banco de Dados
- O modelo de dados é representado pela classe Veiculo no arquivo principal. Aqui estão os campos da tabela:

- id: Chave primária do veículo.
- nome: Nome do veículo.
- marca: Marca do veículo.
- modelo: Modelo do veículo.
- foto: URL ou caminho para a foto do veículo.
- valor: Valor do veículo.
- quilometro: Quilometragem do veículo.

# Autenticação
- O projeto inclui um sistema básico de autenticação com geração de token JWT. Você pode fazer login usando o endpoint /login com as credenciais de exemplo ('usuario@email.com' e 'senha123').

# Endpoints
- GET /veiculos: Retorna a lista de todos os veículos.
- GET /veiculos/{veiculo_id}: Retorna os detalhes de um veículo específico.
- POST /veiculos: Cria um novo veículo com base nos dados fornecidos no corpo da requisição.
- PUT /veiculos/{veiculo_id}: Atualiza os dados de um veículo existente.
- DELETE /veiculos/{veiculo_id}: Exclui um veículo com base no ID fornecido.

# Executando o Aplicativo
- python app.py


# Telas
- Tela de login
  
![image](https://github.com/alansouza19/python-angular-crud/assets/87431289/ac41af84-e73a-4392-9e35-33d829b7a890)


- Home com a lista de veículos cadastrados
  
![image](https://github.com/alansouza19/python-angular-crud/assets/87431289/793e02ed-897d-4ba4-acd0-1b0e2f566dfa)


- Tela de cadastro/atualizar veículo
  
![image](https://github.com/alansouza19/python-angular-crud/assets/87431289/d6f50d7b-2939-4486-a1e9-7e31da28d9c8)




