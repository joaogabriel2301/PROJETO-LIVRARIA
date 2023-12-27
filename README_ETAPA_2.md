## ETAPA 2 --- PROJETO LIVRARIA
Inicialmente, criamos as tabelas, as quais receberam os seus atributos próprios. Analisando a tabela vê-se que cada uma delas contém um id que atuará como chave primária, as quais foram sublinhadas. 

**Tb_Categoria** (Id_categoria, tipo);

**Tb_Clientes** (Id_cliente, nome_cliente, endereco);

**Tb_Autor** (Id_autor, nome_autor, quant_livro_publi);

**Tb_Livros** (Id_livro, ano_publicacao, nome_livro, preco);

<p style="text-align: justify;">
Durante a transformação é possível notar que existe um relacionamento entre a tabela “Tb_Livros” e as tabelas “Tb_Categoria” e “Tb_Autor”. Devido a cardinalidade 1:N desenvolveu-se a estratégia de adição de coluna. Observe-se que adicionou-se à tabela “Tb_Livros” referências com a tabela autor e categoria por meio, respectivamente, do ‘id_autor’ e ‘id_categoria’. Veja abaixo:
</p>

**Tb_Livros** (Id_livro, Id_autor, Id_categoria, ano_publicacao, nome_livro, preco);
<p style="padding-left: 70px;">
    Id_autor referencia Tb_Autor; <br>
	Id_categoria referencia Tb_Categoria;
</p>
<p style="text-align: justify;">
Analisando as tabelas, é notável que existe um relacionamentos entre a tabela “Tb_Livros” e a tabela “Tb_Clientes”  de modo a ser necessário desenvolver a tabela “Tb_Compras”, já que trata-se de uma loja. Assim, criou-se a tabela própria com os atributos mostrados abaixo devido à cardinalidade N:N. 
</p>

**Tb_Compras** (Id_compra, Id_livro, Id_cliente, data_compra, forma_pagamento);
<p style="padding-left: 89px;">
Id_livro referencia Tb_Livros;
<br>
Id_cliente referencia Tb_Clientes;
</p>

Logo, como resultado final, tem-se a seguinte transformação e formação das tabelas: 

**Tb_Categoria** (Id_categoria, tipo);

**Tb_Clientes** (Id_cliente, nome_cliente, endereco);

**Tb_Autor** (Id_autor, nome_autor, quant_livro_publi);

**Tb_Livros** (Id_livro, Id_autor, Id_categoria, ano_publicacao, nome_livro, preco);
<p style="padding-left: 70px;">
Id_autor referencia Tb_Autor;
<br>
Id_categoria referencia Tb_Categoria;
</p>

**Tb_Compras** (Id_compra, Id_livro, Id_cliente, data_compra, forma_pagamento);
<p style="padding-left: 85px;">
Id_livro referencia Tb_Livros;
<br>
Id_cliente referencia Tb_Clientes;
</p>