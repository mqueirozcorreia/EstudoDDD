O repository pattern busca ter uma abstração (ajudando no desacoplamento) da camada de dados, aproximando o uso com o conceito de coleções.

Pode ser usado em conjunto com o Unit of Work, para maior controle de transações.

#Consultas
É possível ter várias formas de consultar a coleção e várias abordagens para atender as necessidades:

..* ter um método list, que recebe um expression, permitindo muita flexibilidade nas consultas, mas menor reaproveitamento
..* criar métodos para cada diferente de consulta a ser realizada, tendo alto reaproveitamenteo, mas ficando complexo o código
..* utilizar o Specification Data Pattern para criar reutilização de partes de consultas, combina-las e controlar entidades relacionadas que serão lidas ou não

#Colunas retornadas
Achei poucas informações de como ter maior controle das colunas selecionadas e até entidades relacionadas carregadas. 

Retornar um IQueryable permite uma forma de definir quais campos retornar na consulta em banco (ao invés de fazer em memória que teve um custo desnecessário), mas pode fazer com quem consumta o repository faça filtros(queries) sem usar o que falei nos itens anteriores.

Fontes:
http://deviq.com/repository-pattern/
http://deviq.com/specification-pattern/