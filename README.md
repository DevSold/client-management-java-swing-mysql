Este projeto é uma aplicação Java desktop com interface gráfica (Swing) para cadastro de clientes, utilizando banco de dados MySQL.

## Funcionalidades

- Adicionar cliente
- Listar clientes
- Buscar cliente por ID
- Buscar cliente por CPF
- Atualizar dados do cliente
- Excluir cliente
- Exportar dados para CSV

## Requisitos

- Java 8+
- MySQL
- Driver JDBC (mysql-connector-j)

## Como Executar

1. Crie o banco de dados no MySQL:
```
CREATE DATABASE cadastro_clientes;
```

2. Crie a tabela:
```
CREATE TABLE clientes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    cpf VARCHAR(14) UNIQUE,
    email VARCHAR(100)
);
```

3. Compile:
```
javac -cp lib/mysql-connector-j-9.3.0.jar -d bin src/**/*.java
```

4. Execute:
```
java -cp "bin;lib/mysql-connector-j-9.3.0.jar" view.ClienteGUI
```

## Autor

cadastro-clientes/
├── src/
│   ├── model/         # Classe Cliente
│   ├── service/       # ClienteDAO (acesso ao banco)
│   ├── view/          # Interface Swing
├── lib/               # mysql-connector
├── bin/               # Arquivos compilados
└── README.md


Projeto criado por Rodrigo Amaral

