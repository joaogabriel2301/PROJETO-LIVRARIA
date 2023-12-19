PROJETO: LIVRARIA
DISCENTES:
- Ana Lívia dos Santos Araújo 20211214010015
- Gabriela de Sousa Oliveira 20221214010032
- João Gabriel de Araújo Oliveira 20211214010019
RESUMO:
O desenvolvimento de um software responsável por gerenciar as
demandas de cadastro e mapeamento das vendas de uma livraria é o objetivo
principal do projeto em andamento. Procura-se desenvolver, aliado ao banco de
dados, a capacidade de administrar a livraria através do cadastro de cada livro
pertencente ao estoque, bem como cada cliente, a fim de conseguir identificar
todas as atividades realizadas pelo setor de vendas em questão. Com isso,
pretende-se desenvolver dentro do projeto o cadastramento dos produtos(livros)
relacionando com sua categoria, autor e código, o registro do cliente e a gestão
de vendas, a qual irá trazer, em linhas gerais, o acompanhamento e a
atualização da loja com segurança dos dados.
EXPLICAÇÃO DO MODELO:
Na abordagem do modelo relacional, busca-se o registro dos livros na
entidade 'livros', a qual está vinculada, por meio de um relacionamento, a outras
duas entidades que a definem: 'categorias’(TIPO) e
'autor'(QUANT_LIVRO_PUBLIC e NOME_AUTOR). Para o cadastro de clientes,
foi criada a entidade 'clientes' (com os campos ENDEREÇO e NOME_CLIENTE).
O relacionamento das vendas ocorre pela ligação entre a entidade 'livros' e a
entidade 'clientes' por meio do relacionamento ‘compras’ (DATA_COMPRA e
FORMA_PAGAMENTO), atualizando tanto o estoque quanto as compras
associadas a cada cliente.
