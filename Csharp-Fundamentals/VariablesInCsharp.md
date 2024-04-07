## literal values ​​and variables in C#

### O que é uma variavel?

Uma *variável* é um contêiner para armazenar um tipo de valor. As variáveis são importantes porque seus valores podem mudar ou variar durante a execução do programa. As variáveis podem ser atribuídas, lidas e alteradas. Use variáveis para armazenar os valores que pretende usar em seu código.

### Como declarar uma variável ?

Para criar uma variável, primeiro você deve declarar o tipo de dados que ela armazenará, depois dar um nome a ela. O nome de uma váriavel deve ser relacionado com a função que ela está representando *(Isso não é obrigatório, mas é uma boa prática)*, além disso, ela também deve ser escrita em **Camel case** *(mais uma vez, é uma boa prática)*.
*Exemplo de como uma variável deve ser declarada*
**Forma errada** -->  `string x;`
**Forma correta** --> `string primeiroNome;`
Neste exemplo, nossa váriavel é do tipo *string* e tem a função de armazenar o primeiro nome de uma pessoa, observa-se que no primeiro exemplo, a variável declarada de `x` não indica para o que ela serve, é apenas uma letra qualquer, dificultando o entendimento do código, entretanto, no segundo exemplo observamos que a variável foi declarada como `primeiroNome`, dessa maneira sabemos para o que essa vaiável serve, conseguindo identificar de maneira imediata a sua funcionalidade.

### Regras e convenções para nomes de variáveis

Para nomes de variáveis em C#, existem algumas regras e convenções que devem ser seguidas:

- Os nomes podem conter letras, números e sublinhados, mas não caracteres especiais como # ou $.
- Devem começar com uma letra alfabética ou sublinhado.
- Distinguem maiúsculas de minúsculas.
- Não podem ser palavras-chave da linguagem.
- Há convenções de codificação que facilitam a leitura do código, como usar camelCase para nomes de variáveis.
- Os nomes devem ser descritivos e sugestivos, representando o tipo de dados que a variável armazena.
- Devem evitar abreviações ou contrações para garantir clareza e compreensão por outros desenvolvedores.
Portanto, ao escolher um nome para uma variável em C#, como no exemplo `string primeiroNome`, é importante seguir essas regras e convenções para manter o código organizado, legível e fácil de entender. Isso é especialmente relevante em projetos maiores, onde a clareza e a consistência são essenciais para a manutenção e colaboração eficientes. 
É importante observar que a atribuição ocorre da direita para a esquerda. Em outras palavras, o compilador do C# deve primeiro entender o valor no lado direito do operador de atribuição e, em seguida, ele pode executar a atribuição à variável no lado esquerdo do operador de atribuição. Se inverter a ordem, você confundirá o compilador de C#.


`O que é Camel case?`
`Camel case é um estilo de nomenclatura de texto usado em programação que combina várias palavras em uma única palavra, em que a primeira letra de cada palavra é escrita em minúscula, exceto a primeira palavra. Por exemplo, se quisermos nomear uma variável que represente a idade de uma pessoa, podemos chamá-la de "idadeDaPessoa" em camel case. Em C#, a convenção de nomenclatura camel case é usada para nomear variáveis, parâmetros de método e propriedades. Embora não seja um requisito absoluto, é considerado uma boa prática seguir esta convenção para manter a consistência e a legibilidade do código.`

### Exemplos de nomes de variáveis

`char userOption;` 
`int gameScore;`
`decimal particlesPerMillion;`
`bool processedCustomer;`

### Atribuir um valor inadequado a uma variável

C# foi projetado para impor tipos. Ao trabalhar com variáveis, a imposição de tipos significa que você não pode atribuir um valor de um tipo de dados a uma variável declarada para conter outro tipo de dados diferente.
**Exemplo:**
`int primeiroNome;`
`primeiroNome = "samuel";`
No exemplo mostrado, se você tentar executar esse código, o C# irá tentar "converter implicitamente" a cadeia de caracteres "Bob" para ser um valor int. No entanto, isso é impossível. Mesmo assim, o C# tenta fazer a conversão, mas irá falhar, pois não há equivalente numérico para a palavra "Bob".

### Reatribuir o valor de uma variável

Você pode reutilizar e reatribuir a variável quantas vezes desejar. Este exemplo ilustra essa ideia.

`string primeiroNome;`
`primeiroNome ="Samuel";`
`Console.WriteLine(primeiroNome);`
`primeiroNome = "Marina";`
`Console.WriteLine(primeiroNome);`

### Inicializar a variável

Você deve atribuir um valor a uma variável antes de poder recuperar o valor dela. Caso contrário, você verá um erro.
**Exemplo:**
`string primeiroNome = "Samuel";`
`Console.WriteLine(primeiroNome);`

###  Variáveis locais de tipo implícito

Uma variável local de tipo implícito é criada usando a palavra-chave var seguida de uma inicialização de variável. Por exemplo:
`var message = "Hello world!";`
Neste exemplo, uma variável de cadeia de caracteres foi criada usando a palavra-chave var em vez da palavra-chave string.
A palavra-chave var informa ao compilador C# que o tipo de dados está implícito pelo valor atribuído. Depois que o tipo é implícito, a variável age da mesma forma como se o próprio tipo de dados real tivesse sido usado para declará-lo. A palavra-chave var é usada para salvar em pressionamentos de tecla quando os tipos são longos ou quando o tipo é óbvio no contexto.
É importante ressaltar que, **as variáveis que usam a palavra-chave *var* devem ser inicializadas**, pois se tentar usar a palavra-chave var sem inicializar a variável, você receberá um erro quando tentar compilar seu código.

### Por que usar a palavra-chave var?

A palavra-chave var foi amplamente adotado na comunidade C#. É provável que se você vir um exemplo de código em um livro ou online, verá a palavra-chave var usada em vez do nome do tipo de dados real. Portanto, é importante entender seu uso.
A palavra-chave var tem um uso importante em C#. Muitas vezes, o tipo de uma variável é óbvio com base em sua inicialização. Nesses casos, é mais simples usar a palavra-chave var. A palavra-chave var também pode ser útil ao planejar o código para um aplicativo. Ao começar a desenvolver um código para uma tarefa, talvez você não saiba imediatamente qual tipo de dados usar. Usar var pode ajudr você a desenvolver sua solução de maneira mais dinâmica.