## Program Strutucture

> Os programas C# podem consistir em um ou mais arquivos. Cada arquivo pode conter zero ou mais namespaces. Um namespace pode conter tipos como classes, estruturas, interfaces, enumerações e delegados, além de outros namespaces. Veja a seguir o esqueleto de um programa em C# que contém todos esses elementos.
    `// A skeleton of a C# program
    using System;
    // Your program starts here:
    Console.WriteLine("Hello world!");
    namespace YourNamespace
    {
        class YourClass
        {
        }
        struct YourStruct
        {
        }
        interface IYourInterface
        {
        }
        delegate int YourDelegate();
        enum YourEnum
        {
        }
        namespace YourNestedNamespace
        {
            struct YourStruct
            {
            }
        }
    }`
    O exemplo anterior usa instruções de nível superior para o ponto de entrada do programa. Esse recurso foi adicionado no C# 9. Antes do C# 9, o ponto de entrada era um método estático chamado Main, como mostra o exemplo a seguir:
    `// A skeleton of a C# program
    using System;
    namespace YourNamespace
    {
        class YourClass
        {
        }
        struct YourStruct
        {
        }
        interface IYourInterface
        {
        }
        delegate int YourDelegate();
        enum YourEnum
        {
        }
        namespace YourNestedNamespace
        {
            struct YourStruct
            {
            }
        }
        class Program
        {
            static void Main(string[] args)
            {
                //Your program starts here...
                Console.WriteLine("Hello world!");
            }
        }
    }`

==========================================================
