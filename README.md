# Introdução
Padrões de projetos são excelentes formas de aplicar soluções validadas para problemas conhecidos.

De toda forma, aplicar soluções onde não existe ou existirá o problema, pode gerar um custo grande no desenvolvimento. A arquitetura emergente fala um pouco disso, de entender que a arquitetura é algo que evolui com o sistema, assim como o negócio.

Tenho percebido uma tentativa de aplicação abrangente de padrões para atender o DDD, com todas as camadas de abstração, em todo e qualquer caso. A dúvida é se o custo x benefício de manter esta abstração desde a concepção do sistema não se torna mais caro do que evoluir ao longo da vida do sistema com refatorações.

Repare, o objetivo não é deixar de ter padrões de projetos, mas sim saber escolher os necessários para cada caso. Assim como o ágil mudou a forma de entregar valor os usuários, ao invés de especificar tudo, codificar tudo, entregar tudo como no waterfall, o mesmo raciocínio se aplica para arquitetura. Deveríamos mesmo fazer a arquitetura completa? Ou ter uma visão de arquitetura e deixar o sistema possível de adicionar novas padrões, quando o desafio for encontrado? E entender que eventuais refatorações são necessárias?

Uma coisa é fato, ter um arquiteto fora do time é como ter área de desenvolvimento separada do teste. As pessoas interagem menos, tomam decisões sem pensar no todo e podem ter um custo maior para manter decisões impostas.

# O que não é?
Como disse o Eduardo Pires "O DDD não é uma receita pronta sobre como desenvolver uma arquitetura baseada em Presentation, Services, Application, Domain e Infra." [3]

# Quando usar DDD
Gosto muito deste texto da Graziella Bonizi da Lambda3
"O DDD é voltado para domínios complexos, e depende da quebra de barreiras de comunicação entre especialistas de negócio e especialistas técnicos, além do engajamento do time técnico em programar de forma que o código reflita o domínio. Se uma dessas variáveis for negativa, provavelmente o DDD não serve para o cenário que você está lidando." [1]

# Arquitetura Emergente
É importante também perceber que não se deve aplicar o DDD em todo o projeto. Deve-se buscar quais as entidades mais importantes para o negócio e entender aquelas mais simples, como um CRUD.

Veja o exemplo abaixo:
![Separação de domínio principal, auxiliar - o que será implementado e integrado](https://www.lambda3.com.br/wp-content/uploads/2017/10/ddd_aplicado_-600x300.png)

Repare que as entidades simples, cadastrais, pode ter uma arquitetura de CRUD muito mais simples que aplicar as camadas do DDD.

Dicas interessantes de um segundo artigo da Graziella da Lambda3  [2]:
"princípios utilizados na implementação do sistema Produção:

**Começar simples**: Você não precisa aplicar todo o conhecimento técnico que você adquiriu na vida de ... evitar causar uma complexidade técnica acidental. Um sistema raramente vai começar com uma arquitetura de microsserviços, por exemplo;
**Não se apegar a Patterns e recursos enquanto eles não forem necessários**:... é importante identificar em conjunto com o time que recursos atenderão melhor o domínio, e não mostrar um apego exagerado a certos recursos / frameworks antes de entender se eles realmente representam um ganho para o projeto;
**Aproveitar as oportunidades de melhoria**: Pode ser que, após diversas interações, o time tenha amadurecido o suficiente para ver que a implementação está limitando o crescimento do projeto. Bom, talvez tenha chegado a hora de refatorar parte, ou até mesmo todo o código."

Eduardo Pires também comenta que não é necessário implementar todas as camadas para ter o DDD:
"O DDD não prega a necessidade de uma arquitetura de 4 camadas (Presentation, Application, Domain e Infra). Pelo contrário, o arquiteto tem a liberdade de definir o melhor estilo arquitetural para atender a necessidade da aplicação, podendo utilizar modelos simples de 3 camadas como o Table Module Pattern."[3]

# Implementações
Uma implementação muito conhecida para .net é o ASP.NET Boilerplate, que tem a implementação das 4 camadas para o DDD:

"Presentation Layer: Provides an interface to the user. Uses the Application Layer to achieve user interactions.
Application Layer: Mediates between the Presentation and Domain Layers. Orchestrates business objects to perform specific application tasks.
Domain Layer: Includes business objects and their rules. This is the heart of the application.
Infrastructure Layer: Provides generic technical capabilities that support higher layers mostly using 3rd-party libraries." [4]

![ASP.NET Boilerplate Application Architecture Model](https://raw.githubusercontent.com/aspnetboilerplate/aspnetboilerplate/master/doc/WebSite/images/abp-nlayer-architecture.png)



# Fontes
[0] [Livro "Domain-Driven Design: Tackling Complexity in the Heart of Software (Inglês)" do Eric Evans (Autor)] (http://amzn.to/2G1o9mZ)
[1] https://www.lambda3.com.br/2017/10/desmistificando-o-ddd/
[2] https://www.lambda3.com.br/2017/11/ddd-aplicado-case-fluxo-de-producao-de-equipamentos-por-demanda/
[3] http://www.eduardopires.net.br/2016/08/ddd-nao-e-arquitetura-em-camadas/
[4] https://aspnetboilerplate.com/Pages/Documents/NLayer-Architecture
https://www.pluralsight.com/courses/domain-driven-design-fundamentals
https://www.lambda3.com.br/2016/10/podcast-14-domain-driven-design/

