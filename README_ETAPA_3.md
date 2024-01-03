## TEXTO ETAPA 3:
CRIAÇÃO DAS TABELAS:
Tb_Categoria (Id_categoria, tipo);

Tb_Clientes (Id_cliente, nome_cliente, endereco);

Tb_Autor (Id_autor, nome_autor, quant_livro_publi);

Tb_Livros (Id_livro, Id_autor, Id_categoria, ano_publicacao, nome_livro, preco);
    <br>
	Id_autor referencia Tb_Autor;
    <br>
	Id_categoria referencia Tb_Categoria;

Tb_Compras (Id_compra, Id_livro, Id_cliente, data_compra, forma_pagamento);
    <br>
	Id_livro referencia Tb_Livro;
    <br>
	Id_cliente referencia Tb_Cliente;

**1FN:**
<br>
<p>
Após a criação das tabelas iniciou-se a primeira etapa da normalização(1FN). Nessa etapa, destrinchamos na tabela “Tb_Clientes” o atributo composto “endereço” em “rua, bairro, num_residencia, cidade, CEP, país”. 
</p>
Tb_Categoria (Id_categoria, tipo);
<br>
Tb_Clientes (Id_cliente, nome_cliente, rua, bairro, num_residência, cidade, CEP, país);

Tb_Autor (Id_autor, nome_autor, quant_livro_publi);

Tb_Livros (Id_livro, Id_autor, Id_categoria, ano_publicação, nome_livro, preço);
	<br>
    Id_autor referencia Tb_Autor;
	<br>
    Id_categoria referencia Tb_Categoria;

Tb_Compras (Id_compra, Id_livro, Id_cliente, data_compra, forma_pagamento);
    <br>
	Id_livro referencia Tb_Livro;
	<br>
    Id_cliente referencia Tb_Cliente;

**2FN:**
<p>
Nessa etapa, devemos analisar a dependência entre os atributos, caso exerça uma dependência total, ou seja, dependência na chave primária, permanece na tabela caso não deve-se analisar a possibilidade de criação de uma nova tabela. Com isso, percebe-se que todos os atributos apresentam uma dependência total, não se aplicando novas modificações.  
</p>
Tb_Categoria (Id_categoria, tipo);

Tb_Clientes (Id_cliente, nome_cliente, rua, bairro, num_residência, cidade, CEP, país);

Tb_Autor (Id_autor, nome_autor, quant_livro_publi);

Tb_Livros (Id_livro, Id_categoria, Id_autor, ano_publicação, nome_livro, preço);
	<br>
    Id_autor referencia Tb_Autor;
    <br>
	Id_categoria referencia Tb_Categoria;
	
Tb_Compras (Id_compra, Id_livro, Id_cliente, data_compra, forma_pagamento);
    <br>
	Id_livro referencia Tb_Livro;
    <br>
	Id_cliente referencia Tb_Cliente;

**3FN:**
<p>
Criou-se uma nova tabela “Tb_Endereco” contendo os atributos que, anteriormente, pertenciam a tabela “Tb_Clientes” e para referenciar a mesma desenvolveu-se um “Id_endereço na tabela clientes. Essa compreende a modificação principal desta etapa.  
</p>

Tb_Categoria (Id_categoria, tipo);

Tb_Clientes (Id_cliente, nome_cliente, Id_endereco);
    <br>
	Id_endereco referencia Tb_Endereco;

Tb_Autor (Id_autor, nome_autor, quant_livro_publi);

Tb_Livros (Id_livro, Id_categoria, Id_autor, ano_publicação, nome_livro, preço);
    <br>
	Id_autor referencia Tb_Autor;
    <br>
	Id_categoria referencia Tb_Categoria;
	
Tb_Compras (Id_compra, Id_livro, Id_cliente, data_compra, forma_pagamento);
    <br>
	Id_livro referencia Tb_Livro;
    <br>
	Id_cliente referencia Tb_Cliente;

Tb_Endereco(Id_endereco, rua, bairro, num_residência, cidade, CEP, país)
    <br>
	Id_endereco referencia Tb_Clientes;
