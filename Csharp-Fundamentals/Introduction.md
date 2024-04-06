##An escape sequence of characters

Uma sequência de caracteres de escape é uma instrução especial para que o runtime insira um caractere especial que afetará a saída da cadeia de caracteres. Em C#, a sequência de caracteres de escape começa com uma barra invertida \ seguida pelo caractere que será escapado. Por exemplo, a sequência *\n* adicionará uma nova linha e uma sequência *\t* adicionará uma guia.
E se você precisar inserir uma aspa dupla em uma cadeia de caracteres literal? Se você não usar a sequência de escape de caracteres, confundirá o compilador, pois ele achará que você deseja terminar a cadeia de caracteres prematuramente. O compilador não entenderá a finalidade dos caracteres após a segunda aspa dupla. Para lidar com isso, use a sequência de escape *\"*
E se você precisar usar a barra invertida para outras finalidades, como exibir um caminho de arquivo?
O problema é a sequência *\s* *\r* não produz um erro porque é uma sequência de escape válida para um retorno de carro. No entanto, não é recomendado usar um retorno de carro neste contexto.

Para resolver o problema, use *\\* para exibir uma barra invertida simples.

###Literal de cadeia de caracteres verbatim
Um literal de cadeia de caracteres textual manterá todo o espaço em branco e os caracteres sem a necessidade de escapar da barra invertida. Para criar uma cadeia de caracteres textual, use a diretiva @ antes da cadeia de caracteres literal.