##Introdução
Padrões de projetos são excelentes formas de aplicar soluções validadas para problemas conhecidos.

De toda forma, aplicar soluções onde não existe ou existirá o problema, pode gerar um custo grande no desenvolvimento. A arquitetura emergente fala um pouco disso, de entender que a arquitetura é algo que evolui com o sistema, assim como o negócio.

Tenho percebido uma tentativa de aplicação abrangente de padrões para atender o DDD, com todas as camadas de abstração, em todo e qualquer caso. A dúvida é se o custo x benefício de manter esta abstração desde a concepção do sistema não se torna mais caro do que evoluir ao longo da vida do sistema com refatorações.

Repare, o objetivo não é deixar de ter padrões de projetos, mas sim saber escolher os necessários para cada caso. Assim como o ágil mudou a forma de entregar valor os usuários, ao invés de especificar tudo, codificar tudo, entregar tudo como no waterfall, o mesmo raciocínio se aplica para arquitetura. Deveríamos mesmo fazer a arquitetura completa? Ou ter uma visão de arquitetura e deixar o sistema possível de adicionar novas padrões, quando o desafio for encontrado? E entender que eventuais refatorações são necessárias?

Uma coisa é fato, ter um arquiteto fora do time é como ter área de desenvolvimento separada do teste. As pessoas interagem menos, tomam decisões sem pensar no todo e podem ter um custo maior para manter decisões impostas.

#Quando usar DDD
Gosto muito deste texto da Graziella Bonizi da Lambda3
"O DDD é voltado para domínios complexos, e depende da quebra de barreiras de comunicação entre especialistas de negócio e especialistas técnicos, além do engajamento do time técnico em programar de forma que o código reflita o domínio. Se uma dessas variáveis for negativa, provavelmente o DDD não serve para o cenário que você está lidando." [1]

##Arquitetura Emergente

#Fontes
[1] https://www.lambda3.com.br/2017/10/desmistificando-o-ddd/
[2] https://www.lambda3.com.br/2017/11/ddd-aplicado-case-fluxo-de-producao-de-equipamentos-por-demanda/
https://www.pluralsight.com/courses/domain-driven-design-fundamentals
https://www.lambda3.com.br/2016/10/podcast-14-domain-driven-design/
