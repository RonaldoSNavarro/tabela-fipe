## 🔖 Sobre

# Tabela FIPE

Este projeto é uma aplicação Java desenvolvida com o framework Spring Boot para consultar o valor médio de veículos de acordo com a tabela FIPE. A aplicação consome uma API externa para obter os dados e utiliza conceitos avançados de programação Java, como coleções, streams e requisições HTTP.

## Estrutura do Projeto

O projeto está estruturado em diferentes pacotes e classes, cada um desempenhando um papel específico:

### Pacote `br.com.alura.TabelaFipe.model`

Contém as classes de modelo que representam os dados obtidos da API da Tabela FIPE.
- **`Dados`**: Classe record que representa os dados básicos de resposta da API, como código e nome do veículo.
- **`Modelos`**: Classe record que representa os modelos de veículos retornados pela API.
- **`Veiculo`**: Classe record que representa um veículo específico com informações detalhadas como marca, modelo, ano e valor.

### Pacote `br.com.alura.TabelaFipe.principal`

Contém a classe principal da aplicação, responsável pela execução do programa.
- **`Principal`**: Contém o método **`exibeMenu`**: Método que exibe o menu de opções ao usuário e coordena o fluxo da aplicação de acordo com as escolhas do usuário.

### Pacote `br.com.alura.TabelaFipe.services`

Contém as classes responsáveis por consumir a API da Tabela FIPE e converter os dados obtidos para objetos de modelo.
- **`ConsumoApi`**: Classe responsável por fazer as requisições HTTP para a API da Tabela FIPE e obter os dados dos veículos.
- **`ConverteDados`**: Classe que implementa a interface `IConverteDados` e é responsável por converter os dados obtidos da API para os objetos de modelo da aplicação.
- **`IConverteDados`**: Interface que define o contrato para conversão de dados da API para objetos de modelo.

### Classe `TabelaFipeApplication`

- **`TabelaFipeApplication`**: Classe de configuração Spring Boot que inicia o servidor da aplicação e instancia a classe `Principal`.

## Técnicas Utilizadas

- **Spring Boot**: Utilização do framework Spring Boot para facilitar o desenvolvimento de aplicações Java.
- **Maven**: Utilização do Maven como gerenciador de dependências para facilitar o gerenciamento das bibliotecas utilizadas no projeto.
- **Requisições HTTP**: Utilização da biblioteca `HttpClient` para realizar requisições HTTP e consumir a API da Tabela FIPE.
- **Jackson Databind**: Adição da dependência jackson-databind para facilitar a serialização e desserialização de objetos Java para JSON e vice-versa.


## Exemplo de Uso

Após iniciar a aplicação, é possível acessar os endpoints RESTful para consultar informações sobre marcas, modelos e valores de veículos. Por exemplo:
- `GET /api/carros/marcas`: Retorna a lista de marcas de carros disponíveis.
- `GET /api/carros/marcas/{codigo}/modelos`: Retorna a lista de modelos de carros de uma marca específica.
- `GET /api/carros/marcas/{codigoMarca}/modelos/{codigoModelo}/anos`: Retorna a lista de anos de um modelo de carro específico.
- `GET /api/carros/marcas/{codigoMarca}/modelos/{codigoModelo}/anos/{ano}`: Retorna informações sobre um carro específico de acordo com o ano.

# Desenvolvedor

[<img loading="lazy" src="https://avatars.githubusercontent.com/u/134724019?v=4" width=115><br><sub>Ronaldo Navarro</sub>](https://github.com/ronaldosnavarro)