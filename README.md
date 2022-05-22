# Code Challenge - Capital Gains

# Stack do projeto
  
## .NET 6
   A tecnologia utilizada para execução do projeto foi o .NET 6 devido a sua flexibilidade de sistema operacional e também pela sua fácil leitura. Não foi utilizado nenhuma biblioteca especial para as operações matemáticas, somente o "Math.abs" para trabalhar com pontos flutuantes no resultado da taxa.
  
## xUnit
  Biblioteca recomendada de .NET 6 para realizar testes unitários.
  
# Como executar?

Para facilitar a execução na pasta tem um arquivo dockerfile que é só gerar uma imagem e rodar o comando "docker run -it" com o id da imagem.

Caso não queira usar o docker, então primeiro instalar o .NET SDK 6 https://dotnet.microsoft.com/en-us/download/dotnet/6.0.
Depois de instalado executar o comando abaixo na pasta "CapitalGains":
     
     dotnet publish CapitalGains.csproj -c Release -o out
O comando vai criar uma pasta "out" com o arquivo "CapitalGains.exe", então é somente executar e começar a testar.

Exemplo da entrada (pressionar enter para confirmar entrada):
   
    [{'operation':'buy', 'unit-cost':10.00, 'quantity': 1000},{'operation':'sell', 'unit-cost':50.00, 'quantity': 15},{'operation':'sell', 'unit-cost':50.00, 'quantity': 15}]


# Estrutura do projeto

  ## Projeto CapitalGains
  
- ### ProgramBase.cs 
    Classe responsável pelo tratamento de input/output do console do executavel.
- ### Program.cs
    Classe principal responsável pela incialização do executavel e orquestração dos métodos.

- ### Service/OperationService.cs
    Classe responsável pelas regras que opera a compra e venda de ações.

- ### Models
    Pasta com os modelos de objetos para tratar entrada e saída de informação do console.

# Testes unitários
- ### CapitalGainsTest
    Contém todos os testes com os casos do documento do desafio.

