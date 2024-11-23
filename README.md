# Rocketseat - Evento: Curso Gratuito de Java 

***Educator: Fernanda Kipper***

Projeto do curso

O projeto trata-se de um sistema de encurtamento de URLs utilizando a AWS como infraestrutura serverless. O objetivo é permitir que os usuários criem URLs curtas que redirecionem para URLs originais, com um tempo de expiração configurável. O sistema é composto por duas funções Lambda: a primeira função é responsável por gerar e armazenar os links encurtados em um bucket S3, junto com informações como a URL original e o tempo de expiração; a segunda função gerencia o redirecionamento, verificando o código da URL curta e validando se a URL ainda está dentro do prazo de expiração antes de redirecionar o usuário.

**Aula 01 - Criando Função Serverless e Configurando URL Encurtada**
- [x] Criação da conta na AWS
- [x] Entender o papel das funções serverless
- [x] Criar nossa primeira função (`helloWorld`)(projeto: HelloWorldJava)
    - [x] Configurações por acesso via url HTTPs
    - [x] Alterar handler padrão
    - [x] Teste da função
- [x] Criação da função `CreateShortUrlLambda`
- [x] Lógica para criar URLs encurtadas
    - [x] Configurar projeto
    - [x] Receber requisição
    - [x] Parsear
    - [x] Extrair dados

**Aula 2: Integração com S3**
- [x] Entender o papel do S3 na arquitetura
- [x] Criação do nosso primeiro bucket
- [x] Criar bucket `url-shortener-bucket` (nome do bucket tem que ser único na região...) 
- [x] Conectar função `CreateShortUrlLambda` ao bucket (projeto: CreateUrlLambda)
- [x] Finalizar código
    - [x] Gerar UUID da URL encurtada
    - [x] Salvar JSON na S3
- [x] Teste da função

**Aula 03 - Redirecionamento de URLs e Configuração do API Gateway**
- [x] Criação da função responsável `RedirectShortUrlLambda` pelo redirect (projeto: RedirectUrlShortener)
- [x] Lógica para redirecionar para URL original
    - [x] Configurar projeto
    - [x] Receber requisição
    - [x] Extrair UUID
    - [x] Acessar S3
    - [x] Validar expiration date
    - [x] Redirecionar para URL original
- [x] Teste da função
- [x] Criar API Gateway para concentrar requisições