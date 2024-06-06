# C# Fundamentos

 Repositorio de projetos de fundamento na linguagem C#

# Perguntas e Respostas

### 1. O C# é uma linguagem compilada, tipada e gerenciada, o que isto significa?
C# é uma linguagem compilada, tipada e gerenciada. Isso significa:
- **Compilada**: O código fonte escrito em C# é transformado em código intermediário (IL - Intermediate Language) pelo compilador. Esse código intermediário é, então, compilado em tempo de execução para código de máquina pela CLR (Common Language Runtime).
- **Tipada**: C# é uma linguagem de tipagem forte, o que significa que todas as variáveis e objetos devem ter um tipo declarado (int, string, etc.). Isso permite que muitos erros sejam detectados em tempo de compilação.
- **Gerenciada**: A execução do código é gerenciada pelo CLR, que cuida de tarefas como coleta de lixo (garbage collection), segurança, e gerenciamento de memória.

### 2. O que diferencia uma linguagem compilada de uma interpretada?
- **Linguagem Compilada**: O código fonte é transformado em código de máquina antes da execução. Exemplos: C#, C++, Java.
- **Linguagem Interpretada**: O código é executado linha por linha por um interpretador em tempo de execução. Exemplos: Python, JavaScript, Ruby.
- **Vantagens da Compilada**: Geralmente tem melhor desempenho devido à tradução prévia para código de máquina.
- **Vantagens da Interpretada**: Flexibilidade e facilidade de depuração, já que o código é executado diretamente.

### 3. Explique como o C# funciona
C# funciona da seguinte forma:
1. O código fonte é escrito em arquivos .cs.
2. O compilador C# (csc) compila o código fonte em IL (Intermediate Language).
3. O IL é armazenado em um assembly (DLL ou EXE).
4. Em tempo de execução, o CLR (Common Language Runtime) compila o IL para código de máquina nativo.
5. O CLR gerencia a execução do código, incluindo garbage collection, segurança, e otimizações de desempenho.

### 4. O que é o CLR?
O Common Language Runtime (CLR) é a máquina virtual da plataforma .NET que gerencia a execução de programas escritos em várias linguagens suportadas pela .NET. Suas principais responsabilidades incluem:
- Compilação JIT (Just-In-Time) do IL para código nativo.
- Gerenciamento de memória e garbage collection.
- Segurança e verificação de tipos.
- Suporte para exceções e depuração.

### 5. O que é IL?
Intermediate Language (IL) é um conjunto de instruções de baixo nível gerado pelo compilador de linguagens .NET (como C#). O IL é independente de plataforma e é convertido em código nativo pelo CLR durante a execução. Ele permite que diferentes linguagens .NET interajam e compartilhem bibliotecas.

### 6. O que é um Framework?
Um framework é uma estrutura de software reutilizável que fornece uma base sobre a qual aplicativos específicos podem ser desenvolvidos. Ele inclui bibliotecas de código, APIs, ferramentas e componentes que facilitam o desenvolvimento e a integração de software. Exemplos incluem .NET Framework, Angular, e Spring.

### 7. O que é o .NET?
.NET é uma plataforma de desenvolvimento de software criada pela Microsoft que fornece ferramentas e bibliotecas para construir e executar aplicativos em várias plataformas, incluindo Windows, macOS, Linux, e dispositivos móveis. Ela suporta múltiplas linguagens de programação, como C#, F#, e Visual Basic.

### 8. O que é o .NET Standard?
.NET Standard é uma especificação que define um conjunto de APIs que todas as implementações do .NET devem seguir. Ele permite que os desenvolvedores escrevam bibliotecas que podem ser usadas em diferentes versões do .NET (como .NET Core, .NET Framework, e Xamarin) sem modificações.

### 9. Explique o que é versão semântica
Versão semântica é um sistema de versionamento de software que utiliza um esquema de numeração no formato MAJOR.MINOR.PATCH:
- **MAJOR**: Incrementado para mudanças incompatíveis.
- **MINOR**: Incrementado para funcionalidades compatíveis adicionadas.
- **PATCH**: Incrementado para correções de bugs compatíveis.

### 10. O que significa LTS na versão do software?
LTS (Long-Term Support) significa Suporte de Longa Duração. Versões LTS de software recebem atualizações e suporte por um período estendido, geralmente 3 anos ou mais, garantindo estabilidade e segurança para empresas que dependem de versões específicas.

### 11. O que é um Runtime?
Runtime refere-se ao ambiente onde o código executa. No contexto do .NET, o runtime é o CLR, que fornece os serviços necessários para executar e gerenciar o código, incluindo compilação JIT, garbage collection, e segurança.

### 12. O que é um SDK?
SDK (Software Development Kit) é um conjunto de ferramentas, bibliotecas, documentação e exemplos que ajudam os desenvolvedores a criar aplicativos para uma plataforma específica. O .NET SDK, por exemplo, inclui o compilador, o runtime, e ferramentas de linha de comando para desenvolvimento de aplicativos .NET.

### 13. O que é um CLI?
CLI (Command Line Interface) é uma interface de usuário baseada em texto que permite aos usuários interagir com o software através de comandos digitados em um terminal ou prompt de comando. No .NET, o CLI é utilizado para compilar, executar e gerenciar projetos.

### 14. Cite 3 tipos de projetos que temos no .NET
- **Console Application**: Projetos que produzem aplicativos de linha de comando.
- **Web Application**: Projetos para desenvolver aplicativos web utilizando ASP.NET.
- **Class Library**: Projetos que criam bibliotecas de classes reutilizáveis que podem ser referenciadas por outros projetos.

### 15. O que é uma Solution?
Uma Solution (Solução) é um contêiner para um ou mais projetos no Visual Studio. Ela permite gerenciar, construir e depurar múltiplos projetos juntos, facilitando a organização e o desenvolvimento de aplicativos complexos que consistem em vários componentes.

### 16. Qual comando para executar uma aplicação .NET?
Para executar uma aplicação .NET, utilize o comando:
------------------------
dotnet run
------------------------
Este comando compila a aplicação (se necessário) e, em seguida, a executa. É especialmente útil durante o desenvolvimento, pois permite testar rapidamente as mudanças no código. O comando `dotnet run` procura um arquivo de projeto (.csproj) ou uma solução (.sln) no diretório atual e executa o aplicativo especificado.

### 17. Qual comando para compilar uma aplicação .NET?
Para compilar uma aplicação .NET, utilize o comando:
------------------------
dotnet build
------------------------
Este comando compila o projeto e todas as suas dependências, gerando os binários no diretório `bin`. O comando `dotnet build` processa todos os arquivos do projeto, gerando os assemblies necessários. Você pode especificar configurações adicionais, como a configuração (Debug ou Release) e o framework alvo.

### 18. Qual comando para publicar uma aplicação .NET?
Para publicar uma aplicação .NET, utilize o comando:
------------------------
dotnet publish
------------------------
Este comando compila a aplicação e prepara os arquivos para implantação em um ambiente de produção. Ele gera todos os arquivos necessários, incluindo os binários e dependências, no diretório `publish`. Você pode especificar opções como o diretório de saída, a configuração (Debug ou Release) e o runtime alvo. Exemplos:
------------------------
dotnet publish --configuration Release --output ./publish
------------------------

### 19. Qual nome do método principal de um Console App?
O método principal de um Console App em C# é chamado de `Main`. Este método é o ponto de entrada do aplicativo e deve ter uma das seguintes assinaturas:
------------------------
static void Main(string[] args)
static int Main(string[] args)
static void Main()
static int Main()
------------------------
O método `Main` pode retornar um inteiro para indicar um código de saída para o sistema operacional. O parâmetro `string[] args` permite passar argumentos da linha de comando para o aplicativo.

### 20. O que significa Debug?
Debug é o processo de identificar e corrigir erros ou bugs no software. Envolve a inspeção detalhada do comportamento do programa durante sua execução. Ferramentas de depuração permitem:
- **Breakpoints**: Pausar a execução em pontos específicos do código.
- **Watch**: Monitorar o valor de variáveis e expressões.
- **Step Over/Into**: Executar o código linha por linha para entender o fluxo de execução.
- **Call Stack**: Visualizar a pilha de chamadas para entender a sequência de execução.

### 21. Como executamos uma aplicação .NET em modo Debug?
Para executar uma aplicação .NET em modo Debug, você pode usar um ambiente de desenvolvimento integrado (IDE) como o Visual Studio, onde há um botão específico para iniciar a depuração (geralmente representado por um ícone de "play" com um inseto). Alternativamente, você pode usar o seguinte comando em um terminal, caso tenha configurado um perfil de depuração:
------------------------
dotnet run --configuration Debug
------------------------
Este comando executa a aplicação usando a configuração de Debug, que inclui informações adicionais de depuração e não otimiza o código, facilitando a identificação de problemas.

### 22. Qual a finalidade da pasta Properties?
A pasta `Properties` em um projeto .NET geralmente contém arquivos de configuração específicos do projeto. O arquivo mais comum é o `AssemblyInfo.cs`, que contém metadados sobre o assembly, como versão, informações de copyright e atributos personalizados. Em aplicativos ASP.NET, pode incluir `launchSettings.json`, que define perfis de execução e configurações de ambiente para depuração.

### 23. Qual a finalidade das pastas Bin e Obj?
- **Bin**: Contém os binários (executáveis e DLLs) gerados após a compilação do projeto. Organizado em subdiretórios por configuração (Debug/Release) e framework alvo.
- **Obj**: Contém arquivos temporários usados pelo processo de compilação, como arquivos de objeto intermediário, caches de dependências e metadados do projeto. Essencial para a eficiência do processo de build, pois armazena informações que podem ser reutilizadas em builds subsequentes.

### 24. Quais partes compõem um programa em C#?
Um programa em C# é composto por:
- **Namespaces**: Agrupam logicamente classes e outros tipos para evitar conflitos de nomes.
- **Classes e Interfaces**: Definem tipos e contratos para objetos.
- **Métodos**: Executam ações e contêm lógica de programação.
- **Propriedades e Campos**: Armazenam dados em classes.
- **Atributos e Eventos**: Fornecem informações adicionais e permitem interações entre objetos.

### 25. O que são Namespaces?
Namespaces são contêineres que fornecem um contexto para os identificadores (nomes de classes, interfaces, etc.) no C#. Eles ajudam a organizar grandes projetos e evitar conflitos de nomes. Por exemplo:
------------------------
namespace MeuProjeto
{
    public class MinhaClasse { }
}
------------------------
O uso de namespaces permite que diferentes partes do código usem nomes semelhantes sem colisão, desde que estejam em namespaces diferentes.

### 26. Qual a finalidade do Using?
A diretiva `using` no C# serve para:
- **Importar namespaces**: Permite usar tipos definidos em outros namespaces sem precisar escrever o nome completo do namespace. Exemplo:
------------------------
using System;
Console.WriteLine("Hello World");
------------------------
- **Gerenciamento de recursos**: Quando usada com objetos que implementam a interface `IDisposable`, garante que os recursos sejam liberados corretamente. Exemplo:
------------------------
using (var recurso = new Recurso())
{
    // uso do recurso
}
------------------------

### 27. Qual a diferença entre uma variável e uma constante?
- **Variável**: Um local na memória que pode armazenar dados e cujo valor pode ser alterado durante a execução do programa. Declarada com a sintaxe:
------------------------
int idade = 30;
------------------------
- **Constante**: Um valor que é definido uma vez e não pode ser alterado. Declarada usando a palavra-chave `const`:
------------------------
const int MaximoTentativas = 5;
------------------------

### 28. Cite 3 nomes reservados que temos no C#
Alguns nomes reservados no C# incluem:
- `abstract`: Usado para declarar classes e métodos abstratos.
- `base`: Usado para acessar membros da classe base.
- `catch`: Usado para capturar exceções em um bloco `try-catch`.

### 29. Quais formas temos de comentar código em C#?
Em C#, podemos comentar o código de três maneiras:
- **Comentário de linha única**: Usando `//`. Exemplo:
------------------------
int x = 10; // Este é um comentário de linha única
------------------------
- **Comentário de bloco**: Usando `/* ... */`. Exemplo:
------------------------
/* Este é um
   comentário de bloco */
------------------------
- **Comentário de documentação**: Usando `///` para gerar documentação XML. Exemplo:
------------------------
/// <summary>
/// Este método faz algo.
/// </summary>
public void MeuMetodo() { }
------------------------

### 30. O que são tipos primitivos?
Tipos primitivos são tipos de dados básicos fornecidos pela linguagem. No C#, incluem:
- `int`: Números inteiros.
- `char`: Caractere único.
- `double`: Números de ponto flutuante de precisão dupla.
- `bool`: Valores booleanos (true/false).

### 31. Qual tipo base no .NET?
O tipo base no .NET é o `System.Object`. Todas as classes e tipos em .NET derivam, direta ou indiretamente, de `System.Object`. Isso significa que todos os tipos, sejam eles definidos pelo usuário ou tipos primitivos, herdam métodos fundamentais, como `ToString()`, `Equals()`, `GetHashCode()`, e `GetType()`.

### 32. Dado um var de um número real, qual tipo seria o var?
Quando utilizamos `var` para declarar uma variável que é inicializada com um número real, o tipo inferido pelo compilador será `double`, a menos que se utilize o sufixo `f` ou `m`:
------------------------
var numeroReal = 1.23; // tipo inferido é double
var numeroRealFloat = 1.23f; // tipo inferido é float
var numeroRealDecimal = 1.23m; // tipo inferido é decimal
------------------------

### 33. Dado um var de um número inteiro, qual tipo seria o var?
Quando utilizamos `var` para declarar uma variável que é inicializada com um número inteiro, o tipo inferido pelo compilador será `int`:
------------------------
var numeroInteiro = 123; // tipo inferido é int
------------------------

### 34. Qual a diferença entre char e string?
- **char**: Representa um único caractere Unicode e é declarado utilizando aspas simples. Exemplo:
------------------------
char letra = 'A';
------------------------
- **string**: Representa uma sequência de caracteres Unicode e é declarado utilizando aspas duplas. Exemplo:
------------------------
string palavra = "Hello";
------------------------

### 35. Qual valor padrão do tipo char?
O valor padrão do tipo `char` é o caractere nulo, representado como `'\0'`.

### 36. Qual a diferença entre var e object?
- **var**: Utilizado para inferência de tipo em tempo de compilação. O tipo exato é determinado pelo compilador com base no valor de inicialização. Exemplo:
------------------------
var texto = "Olá"; // tipo inferido é string
------------------------
- **object**: É o tipo base para todos os tipos em .NET e pode armazenar qualquer tipo de dado. No entanto, para utilizar o valor, geralmente é necessário realizar um casting. Exemplo:
------------------------
object qualquerCoisa = "Olá";
string texto = (string)qualquerCoisa;
------------------------

### 37. O que são tipos nulos?
Tipos nulos (nullable types) são tipos que permitem representar todos os valores de seu tipo base mais um valor adicional: `null`. No C#, são declarados utilizando `?`. Exemplo:
------------------------
int? numero = null;
------------------------
Isso é útil para representar dados que podem ou não estar presentes.

### 38. O que são alias? Cite 3 exemplos
Alias são nomes alternativos para tipos no C#. Alguns exemplos incluem:
- `int` para `System.Int32`
- `string` para `System.String`
- `bool` para `System.Boolean`

### 39. O que são conversões implícitas?
Conversões implícitas são aquelas que o compilador realiza automaticamente, sem necessidade de um cast explícito, geralmente porque não há risco de perda de dados. Exemplos incluem:
------------------------
int numero = 123;
double numeroDouble = numero; // conversão implícita de int para double
------------------------

### 40. O que são conversões explícitas?
Conversões explícitas exigem um cast explícito, geralmente porque há risco de perda de dados ou porque o compilador não pode garantir a segurança da conversão. Exemplo:
------------------------
double numeroDouble = 123.45;
int numero = (int)numeroDouble; // conversão explícita de double para int
------------------------

### 41. Qual a diferença entre parse e Convert?
- **Parse**: Métodos estáticos nas classes de tipo primitivo que convertem strings em seus tipos correspondentes. Lançam uma exceção se a conversão falhar. Exemplo:
------------------------
int numero = int.Parse("123");
------------------------
- **Convert**: Métodos que podem converter vários tipos para outros tipos, incluindo strings. Pode lidar com valores nulos e utiliza `IConvertible` para conversões entre tipos não string. Exemplo:
------------------------
int numero = Convert.ToInt32("123");
------------------------

### 42. O que são operadores aritméticos e quais temos no C#?
Operadores aritméticos são usados para realizar operações matemáticas básicas. No C#, incluem:
- `+` (adição)
- `-` (subtração)
- `*` (multiplicação)
- `/` (divisão)
- `%` (módulo)

### 43. O que são operadores de atribuição e quais temos no C#?
Operadores de atribuição são usados para atribuir valores a variáveis. No C#, incluem:
- `=` (atribuição simples)
- `+=` (adição e atribuição)
- `-=` (subtração e atribuição)
- `*=` (multiplicação e atribuição)
- `/=` (divisão e atribuição)
- `%=` (módulo e atribuição)

### 44. O que são operadores de comparação e quais temos no C#?
Operadores de comparação são usados para comparar valores. No C#, incluem:
- `==` (igualdade)
- `!=` (diferença)
- `>` (maior que)
- `<` (menor que)
- `>=` (maior ou igual a)
- `<=` (menor ou igual a)

### 45. O que são operadores lógicos e quais temos no C#?
Operadores lógicos são usados para realizar operações lógicas em valores booleanos. No C#, incluem:
- `&&` (AND lógico)
- `||` (OR lógico)
- `!` (NOT lógico)

### 46. Cite duas estruturas condicionais que temos no C#
Duas estruturas condicionais no C# são:
- **if/else**: Executa um bloco de código se uma condição for verdadeira, e opcionalmente outro bloco se a condição for falsa.
------------------------
if (condicao)
{
    // código se a condição for verdadeira
}
else
{
    // código se a condição for falsa
}
------------------------
- **switch**: Seleciona um bloco de código para executar com base no valor de uma expressão.
------------------------
switch (expressao)
{
    case valor1:
        // código para valor1
        break;
    case valor2:
        // código para valor2
        break;
    default:
        // código padrão
        break;
}
------------------------

### 47. Cite duas estruturas de repetição que temos no C#
Duas estruturas de repetição no C# são:
- **for**: Itera um bloco de código um número específico de vezes.
------------------------
for (int i = 0; i < 10; i++)
{
    // código a ser repetido
}
------------------------
- **while**: Itera um bloco de código enquanto uma condição for verdadeira.
------------------------
while (condicao)
{
    // código a ser repetido
}
------------------------

### 48. Qual a diferença entre while e do/while?
A diferença entre `while` e `do/while` é:
- **while**: Verifica a condição antes de executar o bloco de código.
------------------------
while (condicao)
{
    // código a ser repetido
}
------------------------
- **do/while**: Executa o bloco de código pelo menos uma vez, depois verifica a condição.
------------------------
do
{
    // código a ser repetido
} while (condicao);
------------------------

### 49. Como definimos que um método não retorna valor algum?
Um método que não retorna valor algum é definido usando a palavra-chave `void`. Exemplo:
------------------------
public void MeuMetodo()
{
    // código do método
}
------------------------

### 50. Podemos ter métodos sem parâmetros no C#?
Sim, podemos ter métodos sem parâmetros no C#. Exemplo:
------------------------
public void MeuMetodo()
{
    // código do método
}
------------------------
### 51. Como tornamos um parâmetro opcional no C#?
Para tornar um parâmetro opcional em C#, você pode fornecer um valor padrão para o parâmetro na assinatura do método. Exemplo:
------------------------
public void MeuMetodo(int obrigatorio, int opcional = 10)
{
    // código do método
}
------------------------
Neste exemplo, o parâmetro `opcional` tem um valor padrão de 10, então o método pode ser chamado com um ou dois argumentos.

### 52. O que são heap e stack?
- **Heap**: É uma área de memória usada para armazenar objetos dinamicamente alocados. A alocação e desalocação de memória no heap são gerenciadas pelo Garbage Collector.
- **Stack**: É uma área de memória usada para armazenar variáveis locais e informações de controle de fluxo (como endereços de retorno). O stack segue o modelo LIFO (Last In, First Out).

### 53. O que são tipos de valor e tipos de referência?
- **Tipos de Valor**: Armazenam dados diretamente e são alocados na stack. Exemplos incluem `int`, `char`, e `structs`.
- **Tipos de Referência**: Armazenam uma referência a um local na heap onde os dados reais são armazenados. Exemplos incluem `class`, `interface`, `delegate`, e `arrays`.

### 54. Onde são armazenados os tipos de valor?
Os tipos de valor são armazenados na stack, onde o tempo de vida e o escopo são bem definidos e limitados ao bloco de código em que são definidos.

### 55. Onde são armazenados os tipos de referência?
Os tipos de referência são armazenados na heap, com a referência para esses dados armazenada na stack. Isso permite que os objetos tenham um tempo de vida mais flexível e possam ser compartilhados entre diferentes partes do código.

### 56. O que são Structs?
Structs são tipos de valor que permitem agrupar variáveis relacionadas em uma única unidade. São úteis para representar pequenos conjuntos de dados relacionados. Ao contrário das classes, structs não suportam herança, mas podem implementar interfaces.
------------------------
public struct Ponto
{
    public int X;
    public int Y;
}
------------------------

### 57. O que são enumeradores?
Enumeradores (enums) são tipos de valor que consistem em um conjunto de constantes nomeadas. São usados para representar um grupo de valores relacionados de uma maneira mais legível.
------------------------
public enum DiasDaSemana
{
    Domingo,
    Segunda,
    Terca,
    Quarta,
    Quinta,
    Sexta,
    Sabado
}
------------------------

### 58. O que é um GUID?
GUID (Globally Unique Identifier) é um identificador único globalmente. No C#, ele é representado pela estrutura `System.Guid` e é usado para identificar de maneira única objetos ou registros.
------------------------
Guid id = Guid.NewGuid();
------------------------

### 59. O que é interpolação de String?
Interpolação de string permite a inserção de expressões dentro de literais de string. No C#, é feita utilizando o símbolo `$` antes da string e `{}` para delimitar as expressões.
------------------------
int idade = 30;
string mensagem = $"Eu tenho {idade} anos.";
------------------------

### 60. Qual a finalidade do método CompareTo?
O método `CompareTo` é usado para comparar a instância atual com outro objeto do mesmo tipo e retorna um valor que indica a ordem relativa dos objetos comparados. Retorna:
- **Menor que zero**: Se a instância atual é menor.
- **Zero**: Se são iguais.
- **Maior que zero**: Se a instância atual é maior.
------------------------
int resultado = x.CompareTo(y);
------------------------

### 61. Qual a finalidade do método Contains?
O método `Contains` é usado para verificar se uma determinada substring está presente dentro de uma string.
------------------------
string texto = "Olá, mundo!";
bool contem = texto.Contains("mundo");
------------------------

### 62. Qual a finalidade do método StartsWith e EndsWith?
- **StartsWith**: Verifica se uma string começa com uma determinada substring.
------------------------
string texto = "Olá, mundo!";
bool comecaComOla = texto.StartsWith("Olá");
------------------------
- **EndsWith**: Verifica se uma string termina com uma determinada substring.
------------------------
bool terminaComMundo = texto.EndsWith("mundo!");
------------------------

### 63. Qual a finalidade do método Equals?
O método `Equals` é usado para determinar se duas instâncias de um objeto são iguais. No C#, é frequentemente sobrescrito em classes para fornecer uma comparação específica.
------------------------
public override bool Equals(object obj)
{
    // implementação da comparação
}
------------------------

### 64. Qual a finalidade do método IndexOf e LastIndexOf?
- **IndexOf**: Retorna o índice da primeira ocorrência de uma substring dentro de uma string.
------------------------
string texto = "Olá, mundo!";
int indice = texto.IndexOf("mundo");
------------------------
- **LastIndexOf**: Retorna o índice da última ocorrência de uma substring dentro de uma string.
------------------------
int ultimoIndice = texto.LastIndexOf("o");
------------------------

### 65. Qual a finalidade do método ToLower e ToUpper?
- **ToLower**: Converte todos os caracteres de uma string para minúsculas.
------------------------
string texto = "Olá, Mundo!";
string textoMinusculo = texto.ToLower();
------------------------
- **ToUpper**: Converte todos os caracteres de uma string para maiúsculas.
------------------------
string textoMaiusculo = texto.ToUpper();
------------------------

### 66. Qual a finalidade do método Insert?
O método `Insert` insere uma substring em uma posição específica dentro de uma string.
------------------------
string texto = "Olá, mundo!";
string novoTexto = texto.Insert(4, "querido ");
------------------------
Neste exemplo, "querido " é inserido na posição 4 da string original.

### 67. Qual a finalidade do método Length?
A propriedade `Length` retorna o número de caracteres em uma string.
------------------------
string texto = "Olá, mundo!";
int comprimento = texto.Length;
------------------------

### 68. Qual a finalidade do método Remove?
O método `Remove` remove uma parte de uma string, começando em um índice especificado.
------------------------
string texto = "Olá, mundo!";
string novoTexto = texto.Remove(4, 7);
------------------------
Neste exemplo, a partir do índice 4, 7 caracteres são removidos.

### 69. Qual a finalidade do método Replace?
O método `Replace` substitui todas as ocorrências de uma substring por outra.
------------------------
string texto = "Olá, mundo!";
string novoTexto = texto.Replace("mundo", "amigo");
------------------------

### 70. Qual a finalidade do método Split?
O método `Split` divide uma string em uma matriz de substrings com base em delimitadores especificados.
------------------------
string texto = "Olá, mundo!";
string[] palavras = texto.Split(' ');
------------------------

### 71. Qual a finalidade do método Substring?
O método `Substring` retorna uma nova string que é uma parte da string original, começando em um índice especificado.
------------------------
string texto = "Olá, mundo!";
string novaString = texto.Substring(4, 5);
------------------------

### 72. Qual a finalidade do método Trim?
O método `Trim` remove todos os espaços em branco do início e do final de uma string.
------------------------
string texto = "  Olá, mundo!  ";
string textoTrimmed = texto.Trim();
------------------------

### 73. O que é StringBuilder e quando devemos utilizar?
`StringBuilder` é uma classe usada para manipular dinamicamente strings de maneira eficiente, especialmente quando várias modificações são necessárias. Ao contrário das strings, que são imutáveis, `StringBuilder` permite a modificação de seu conteúdo sem criar novos objetos.
------------------------
StringBuilder sb = new StringBuilder();
sb.Append("Olá");
sb.Append(", mundo!");
string resultado = sb.ToString();
------------------------
Utilize `StringBuilder` quando estiver realizando muitas operações de concatenação para evitar o overhead de criar várias instâncias de strings.

### 74. O que é Regex e quando devemos utilizar?
`Regex` (Expressão Regular) é uma classe usada para realizar operações de correspondência de padrões em strings, como busca, substituição e validação. É útil para validar formatos complexos de entrada, como endereços de e-mail e números de telefone.
------------------------
using System.Text.RegularExpressions;

string padrao = @"^\d{4}-\d{2}-\d{2}$";
string data = "2024-06-06";
bool isMatch = Regex.IsMatch(data, padrao);
------------------------

### 75. O que é o DateTime?
`DateTime` é uma estrutura que representa instantes específicos no tempo, normalmente expressos como uma data e hora do dia. Ela oferece diversos métodos para manipulação e formatação de datas e horas.
------------------------
DateTime agora = DateTime.Now;
DateTime dataEspecifica = new DateTime(2024, 6, 6);
------------------------

### 76. Como obtemos a data de hoje no C#?
Para obter a data de hoje no C#, utilize a propriedade `DateTime.Now`:
------------------------
DateTime hoje = DateTime.Now;
------------------------
Se quiser apenas a data sem a hora, utilize:
------------------------
DateTime hoje = DateTime.Today;
------------------------

### 77. Como convertemos uma data para String?
Para converter uma data para string, utilize o método `ToString` da classe `DateTime` com um formato específico, se desejado.
------------------------
DateTime hoje = DateTime.Now;
string dataString = hoje.ToString("yyyy-MM-dd");
------------------------

### 78. Como comparamos duas datas em C#?
Para comparar duas datas, você pode usar os operadores de comparação (`<`, `>`, `<=`, `>=`) ou os métodos `Compare` e `CompareTo`.
------------------------
DateTime data1 = new DateTime(2024, 6, 6);
DateTime data2 = DateTime.Now;

int comparacao = DateTime.Compare(data1, data2);

if (comparacao < 0)
{
    Console.WriteLine("data1 é anterior a data2");
}
else if (comparacao == 0)
{
    Console.WriteLine("data1 é igual a data2");
}
else
{
    Console.WriteLine("data1 é posterior a data2");
}
------------------------

### 79. Como podemos obter o ano, mês ou dia no C#?
Para obter o ano, mês ou dia de um objeto `DateTime`, utilize as propriedades `Year`, `Month` e `Day`:
------------------------
DateTime hoje = DateTime.Now;
int ano = hoje.Year;
int mes = hoje.Month;
int dia = hoje.Day;
------------------------

### 80. Como podemos obter o último dia do mês no C#?
Para obter o último dia do mês, você pode usar o método `DateTime.DaysInMonth` para encontrar o número de dias em um mês específico e, em seguida, criar uma data com esse valor.
------------------------
int ano = 2024;
int mes = 6;
int ultimoDia = DateTime.DaysInMonth(ano, mes);
DateTime ultimoDiaDoMes = new DateTime(ano, mes, ultimoDia);
------------------------

### 81. Podemos criar datas nulas?
Sim, podemos criar datas nulas usando tipos nulos (nullable types) com `DateTime?`.
------------------------
DateTime? dataNula = null;
------------------------

### 82. O que são nullable types?
Nullable types permitem que tipos de valor (como `int`, `bool`, `DateTime`) armazenem um valor nulo (`null`) além de seus valores normais. São declarados usando `?`.
------------------------
int? numeroNulo = null;
------------------------

### 83. O que é Timezone?
Timezone (fuso horário) representa a diferença de tempo entre uma localização específica e o Tempo Universal Coordenado (UTC). `TimeZoneInfo` é a classe no C# que fornece informações sobre fusos horários.
------------------------
TimeZoneInfo fusoHorario = TimeZoneInfo.Local;
------------------------

### 84. Como obtermos a data sem um Timezone no C#?
Para obter uma data sem um fuso horário específico, use a estrutura `DateTime` sem qualquer conversão para fusos horários:
------------------------
DateTime data = DateTime.Now;
------------------------

### 85. O que é DateTime Offset?
`DateTimeOffset` é uma estrutura que representa uma data e hora com um deslocamento em relação ao UTC. Ele é útil para armazenar e manipular data e hora em diferentes fusos horários.
------------------------
DateTimeOffset agora = DateTimeOffset.Now;
------------------------

### 86. O que é um TimeSpan?
`TimeSpan` é uma estrutura que representa um intervalo de tempo. Pode ser usada para armazenar durações ou calcular a diferença entre duas datas.
------------------------
TimeSpan duracao = new TimeSpan(1, 30, 0); // 1 hora e 30 minutos
------------------------

### 87. Qual a finalidade do Math.Round, Math.Celling e Math.Floor?
- **Math.Round**: Arredonda um número para o inteiro mais próximo.
------------------------
double valor = 3.56;
double arredondado = Math.Round(valor); // 4
------------------------
- **Math.Ceiling**: Arredonda um número para o próximo inteiro maior.
------------------------
double valor = 3.56;
double arredondadoCima = Math.Ceiling(valor); // 4
------------------------
- **Math.Floor**: Arredonda um número para o próximo inteiro menor.
------------------------
double valor = 3.56;
double arredondadoBaixo = Math.Floor(valor); // 3
------------------------

### 88. Qual a diferença entre IEnumerable, IList e ICollection?
- **IEnumerable**: Interface básica para iteração sobre uma coleção. Permite apenas leitura sequencial.
------------------------
IEnumerable<int> numeros = new List<int> { 1, 2, 3 };
foreach (int num in numeros)
{
    Console.WriteLine(num);
}
------------------------
- **ICollection**: Herda de `IEnumerable` e adiciona suporte para contagem de itens, adição e remoção de itens.
------------------------
ICollection<int> colecao = new List<int> { 1, 2, 3 };
int contagem = colecao.Count;
------------------------
- **IList**: Herda de `ICollection` e adiciona suporte para acesso indexado e inserção/remocao de itens em posições específicas.
------------------------
IList<int> lista = new List<int> { 1, 2, 3 };
int primeiroItem = lista[0];
lista.Insert(1, 4);
------------------------

### 89. Qual a diferença entre List e IList?
- **List<T>**: É uma implementação concreta da interface `IList<T>` fornecida pelo .NET Framework. Usada para armazenar coleções de dados que podem ser acessadas por índice e manipuladas de várias maneiras.
- **IList<T>**: É uma interface que define operações de listas indexadas. `List<T>` é apenas uma das implementações possíveis dessa interface.
------------------------
List<int> minhaLista = new List<int> { 1, 2, 3 };
IList<int> listaInterface = minhaLista;
------------------------

### 90. Qual a finalidade do método Add e AddRange em uma lista?
- **Add**: Adiciona um único elemento ao final da lista.
------------------------
List<int> lista = new List<int>();
lista.Add(1);
------------------------
- **AddRange**: Adiciona uma coleção de elementos ao final da lista.
------------------------
List<int> lista = new List<int>();
lista.AddRange(new int[] { 2, 3, 4 });
------------------------

### 91. Qual a finalidade do método Clear em uma lista?
O método `Clear` remove todos os elementos da lista, deixando-a vazia.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
lista.Clear(); // lista agora está vazia
------------------------

### 92. Qual a finalidade do método Contains em uma lista?
O método `Contains` verifica se um elemento específico está presente na lista.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
bool contem = lista.Contains(2); // true
------------------------

### 93. Qual a finalidade do método CopyTo em uma lista?
O método `CopyTo` copia os elementos da lista para uma matriz unidimensional, começando em um índice especificado da matriz de destino.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
int[] array = new int[5];
lista.CopyTo(array, 1); // array agora contém [0, 1, 2, 3, 0]
------------------------

### 94. Qual a finalidade do método Exists em uma lista?
O método `Exists` verifica se algum elemento da lista corresponde a um predicado especificado.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
bool existe = lista.Exists(x => x > 2); // true
------------------------

### 95. Qual a finalidade do método Find e FindAll em uma lista?
- **Find**: Retorna o primeiro elemento que corresponde ao predicado especificado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 4 };
int encontrado = lista.Find(x => x > 2); // 3
------------------------
- **FindAll**: Retorna todos os elementos que correspondem ao predicado especificado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 4 };
List<int> encontrados = lista.FindAll(x => x > 2); // [3, 4]
------------------------

### 96. Qual a finalidade do método IndexOf e LastIndexOf em uma lista?
- **IndexOf**: Retorna o índice da primeira ocorrência de um elemento especificado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 2 };
int indice = lista.IndexOf(2); // 1
------------------------
- **LastIndexOf**: Retorna o índice da última ocorrência de um elemento especificado.
------------------------
int ultimoIndice = lista.LastIndexOf(2); // 3
------------------------

### 97. Qual a finalidade do método FindIndex, FindLast e FindLastIndex em uma lista?
- **FindIndex**: Retorna o índice do primeiro elemento que corresponde ao predicado especificado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 4 };
int indice = lista.FindIndex(x => x > 2); // 2
------------------------
- **FindLast**: Retorna o último elemento que corresponde ao predicado especificado.
------------------------
int ultimoEncontrado = lista.FindLast(x => x > 2); // 4
------------------------
- **FindLastIndex**: Retorna o índice do último elemento que corresponde ao predicado especificado.
------------------------
int ultimoIndice = lista.FindLastIndex(x => x > 2); // 3
------------------------

### 98. Qual a finalidade do método Insert e InsertRange em uma lista?
- **Insert**: Insere um elemento na lista na posição especificada.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
lista.Insert(1, 4); // lista agora contém [1, 4, 2, 3]
------------------------
- **InsertRange**: Insere uma coleção de elementos na lista, começando na posição especificada.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
lista.InsertRange(1, new int[] { 5, 6 }); // lista agora contém [1, 5, 6, 2, 3]
------------------------

### 99. Qual a finalidade do método Remove, RemoveAll, RemoveAt e RemoveRange em uma lista?
- **Remove**: Remove a primeira ocorrência de um elemento especificado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 2 };
lista.Remove(2); // lista agora contém [1, 3, 2]
------------------------
- **RemoveAll**: Remove todos os elementos que correspondem ao predicado especificado.
------------------------
lista.RemoveAll(x => x > 2); // lista agora contém [1, 2]
------------------------
- **RemoveAt**: Remove o elemento na posição especificada.
------------------------
lista.RemoveAt(1); // lista agora contém [1, 3]
------------------------
- **RemoveRange**: Remove uma quantidade especificada de elementos, começando na posição especificada.
------------------------
lista.RemoveRange(1, 2); // lista agora contém [1]
------------------------

### 100. Qual a finalidade do método Reverse em uma lista?
O método `Reverse` inverte a ordem dos elementos na lista.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
lista.Reverse(); // lista agora contém [3, 2, 1]
------------------------

### 101. Qual a finalidade do método Sort em uma lista?
O método `Sort` ordena os elementos da lista em ordem crescente.
------------------------
List<int> lista = new List<int> { 3, 1, 2 };
lista.Sort(); // lista agora contém [1, 2, 3]
------------------------

### 102. Qual a finalidade do método ToArray em uma lista?
O método `ToArray` converte a lista em uma matriz (array).
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
int[] array = lista.ToArray();
------------------------

### 103. Qual a finalidade do método TrueForAll em uma lista?
O método `TrueForAll` verifica se todos os elementos da lista atendem a um predicado especificado.
------------------------
List<int> lista = new List<int> { 2, 4, 6 };
bool todosPares = lista.TrueForAll(x => x % 2 == 0); // true
------------------------

### 104. Qual a finalidade do método ConvertAll em uma lista?
O método `ConvertAll` converte todos os elementos da lista para um novo tipo, aplicando uma função de conversão a cada elemento.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
List<string> strings = lista.ConvertAll(x => x.ToString());
------------------------

### 105. Qual a finalidade do método ForEach em uma lista?
O método `ForEach` executa uma ação específica em cada elemento da lista.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
lista.ForEach(x => Console.WriteLine(x));
------------------------

### 106. Qual a finalidade do método Where em uma lista?
O método `Where` filtra os elementos da lista com base em um predicado especificado, retornando uma nova coleção que contém apenas os elementos que satisfazem o predicado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 4 };
IEnumerable<int> pares = lista.Where(x => x % 2 == 0); // [2, 4]
------------------------

### 107. Qual a finalidade do método First em uma lista?
O método `First` retorna o primeiro elemento da lista que satisfaz um predicado especificado. Lança uma exceção se nenhum elemento for encontrado.
------------------------
List<int> lista = new List<int> { 1, 2, 3, 4 };
int primeiroPar = lista.First(x => x % 2 == 0); // 2
------------------------

### 108. Qual a finalidade do método OrderBy em uma lista?
O método `OrderBy` ordena os elementos da lista em ordem crescente com base em uma chave especificada.
------------------------
List<int> lista = new List<int> { 3, 1, 4, 2 };
IEnumerable<int> ordenada = lista.OrderBy(x => x); // [1, 2, 3, 4]
------------------------

### 109. Qual a finalidade do método Sort em uma lista?
O método `Sort` ordena os elementos da lista em ordem crescente.
------------------------
List<int> lista = new List<int> { 3, 1, 2 };
lista.Sort(); // lista agora contém [1, 2, 3]
------------------------

### 110. Qual a finalidade do método Select em uma lista?
O método `Select` projeta cada elemento de uma coleção em um novo formulário, aplicando uma função de transformação a cada elemento.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
IEnumerable<string> strings = lista.Select(x => x.ToString()); // ["1", "2", "3"]
------------------------
### 111. Qual a finalidade do método Convertendo Listas em uma lista?
Presumo que "Convertendo Listas" se refira ao uso do método `ConvertAll` para converter todos os elementos de uma lista para outro tipo. Este método é útil para transformar uma lista de um tipo em uma lista de outro tipo.
------------------------
List<int> lista = new List<int> { 1, 2, 3 };
List<string> strings = lista.ConvertAll(x => x.ToString());
------------------------

### 112. O que são Classes e Objetos?
- **Classes**: São definições de tipos de dados que encapsulam dados e métodos que operam sobre esses dados. Uma classe é um blueprint a partir do qual objetos são criados.
------------------------
public class Pessoa
{
    public string Nome { get; set; }
    public int Idade { get; set; }
}
------------------------
- **Objetos**: São instâncias de classes. Eles contêm valores concretos e têm comportamento definido pelas classes.
------------------------
Pessoa pessoa = new Pessoa { Nome = "João", Idade = 30 };
------------------------

### 113. O que é uma instância?
Uma instância é um objeto concreto criado a partir de uma classe. Criar uma instância de uma classe é o processo de alocar memória e inicializar um objeto dessa classe.
------------------------
Pessoa pessoa = new Pessoa();
------------------------

### 114. O que são Propriedades?
Propriedades são membros de uma classe que fornecem um mecanismo flexível para ler, gravar ou calcular o valor de um campo particular. Elas são usadas como campos públicos, mas com controle adicional.
------------------------
public class Pessoa
{
    public string Nome { get; set; }
    public int Idade { get; set; }
}
------------------------

### 115. O que são Métodos construtores?
Métodos construtores são métodos especiais de uma classe que são chamados quando uma nova instância da classe é criada. Eles são usados para inicializar objetos.
------------------------
public class Pessoa
{
    public string Nome { get; set; }
    public int Idade { get; set; }

    // Construtor
    public Pessoa(string nome, int idade)
    {
        Nome = nome;
        Idade = idade;
    }
}
------------------------

### 116. O que é o Garbage Collector?
O Garbage Collector (GC) é um mecanismo de gerenciamento automático de memória no .NET que recupera a memória alocada por objetos que não são mais necessários pelo programa. Ele executa a coleta de lixo, que é o processo de identificar e liberar memória usada por objetos que não têm mais referências ativas.

### 117. O que é Object Dispose?
`Dispose` é um método da interface `IDisposable` usado para liberar recursos não gerenciados explicitamente, como conexões de banco de dados, arquivos, etc. Implementar `Dispose` permite liberar esses recursos de forma determinística.
------------------------
public class Recurso : IDisposable
{
    public void Dispose()
    {
        // Liberar recursos
    }
}
------------------------

### 118. Defina os modificadores public, private e protected
- **public**: O membro é acessível a partir de qualquer lugar.
------------------------
public class MinhaClasse
{
    public int MeuCampo;
}
------------------------
- **private**: O membro é acessível apenas dentro da classe em que foi declarado.
------------------------
public class MinhaClasse
{
    private int MeuCampo;
}
------------------------
- **protected**: O membro é acessível dentro da classe em que foi declarado e em classes derivadas.
------------------------
public class MinhaClasse
{
    protected int MeuCampo;
}
------------------------

### 119. O que são objetos estáticos?
Objetos estáticos são instâncias de classes que são únicas no contexto da aplicação. Membros estáticos são compartilhados por todas as instâncias da classe e podem ser acessados diretamente pela classe sem a criação de um objeto.
------------------------
public class MinhaClasse
{
    public static int Contador;
}
------------------------

### 120. O que é Herança?
Herança é um princípio da programação orientada a objetos que permite que uma classe (classe derivada) herde membros (campos, propriedades, métodos) de outra classe (classe base). Isso promove a reutilização de código.
------------------------
public class Animal
{
    public void Comer() { }
}

public class Cachorro : Animal
{
    public void Latir() { }
}
------------------------

### 121. O que é Upcast e Downcast?
- **Upcast**: Converter um objeto de uma classe derivada para uma classe base. É implícito e seguro.
------------------------
Cachorro cachorro = new Cachorro();
Animal animal = cachorro; // Upcast
------------------------
- **Downcast**: Converter um objeto de uma classe base para uma classe derivada. É explícito e pode lançar exceções se o tipo não for compatível.
------------------------
Animal animal = new Cachorro();
Cachorro cachorro = (Cachorro)animal; // Downcast
------------------------

### 122. O que são Interfaces?
Interfaces são contratos que definem um conjunto de métodos e propriedades que uma classe deve implementar. Elas não contêm implementação de código, apenas a assinatura dos membros.
------------------------
public interface IAnimal
{
    void Comer();
}

public class Cachorro : IAnimal
{
    public void Comer() { }
}
------------------------

### 123. O que são Classes abstratas?
Classes abstratas são classes que não podem ser instanciadas diretamente e podem conter métodos abstratos (sem implementação) e métodos concretos (com implementação). Elas são usadas para fornecer uma base para outras classes.
------------------------
public abstract class Animal
{
    public abstract void Comer();
}

public class Cachorro : Animal
{
    public override void Comer() { }
}
------------------------

### 124. Qual a finalidade das Classes seladas?
Classes seladas (sealed) são classes que não podem ser herdadas. Usar `sealed` em uma classe pode melhorar o desempenho, pois o compilador pode fazer otimizações.
------------------------
public sealed class MinhaClasseSelada
{
    // Implementação
}
------------------------

### 125. O que é Sobrecarga de métodos?
Sobrecarga de métodos permite definir múltiplos métodos com o mesmo nome, mas com assinaturas diferentes (diferentes tipos ou número de parâmetros) dentro da mesma classe.
------------------------
public class MinhaClasse
{
    public void Metodo(int x) { }
    public void Metodo(string x) { }
}
------------------------

### 126. O que é Sobrescrita de método?
Sobrescrita de método permite que uma classe derivada forneça uma implementação específica de um método que já está definido na classe base. Usa-se a palavra-chave `override`.
------------------------
public class Animal
{
    public virtual void FazerSom() { }
}

public class Cachorro : Animal
{
    public override void FazerSom()
    {
        Console.WriteLine("Latido");
    }
}
------------------------

### 127. Como podemos Comparar dois objetos no C#?
Para comparar dois objetos no C#, você pode usar o método `Equals` ou sobrecarregar os operadores de igualdade (`==` e `!=`). Também é comum implementar a interface `IComparable` para fornecer uma ordem natural de comparação.
------------------------
public class Pessoa : IComparable<Pessoa>
{
    public string Nome { get; set; }
    public int CompareTo(Pessoa outra)
    {
        return this.Nome.CompareTo(outra.Nome);
    }
}
------------------------

### 128. Qual a finalidade do Dispose?
O método `Dispose` da interface `IDisposable` é usado para liberar recursos não gerenciados, como conexões de banco de dados, arquivos, etc. É implementado para garantir que esses recursos sejam liberados de forma determinística.
------------------------
public class Recurso : IDisposable
{
    public void Dispose()
    {
        // Liberar recursos
    }
}
------------------------

### 129. O que é Encapsulamento?
Encapsulamento é um dos princípios da programação orientada a objetos que consiste em esconder os detalhes internos de uma classe e expor apenas o que é necessário através de métodos e propriedades públicos. Isso melhora a modularidade e a manutenção do código.
------------------------
public class Pessoa
{
    private string nome;
    public string Nome
    {
        get { return nome; }
        set { nome = value; }
    }
}
------------------------

### 130. O que é Polimorfismo?
Polimorfismo é a capacidade de tratar objetos de diferentes tipos de forma uniforme. Isso é alcançado através de herança e interfaces, permitindo que métodos em classes derivadas sejam chamados através de uma referência para a classe base ou interface.
------------------------
public class Animal
{
    public virtual void FazerSom() { }
}

public class Cachorro : Animal
{
    public override void FazerSom()
    {
        Console.WriteLine("Latido");
    }
}

Animal meuAnimal = new Cachorro();
meuAnimal.FazerSom(); // Output: Latido
------------------------

### 131. O que são Tipos complexos?
Tipos complexos são tipos de dados que podem ser compostos por tipos primitivos e outros tipos complexos. No C#, esses incluem classes, structs, arrays, coleções e outros tipos definidos pelo usuário.
------------------------
public class Endereco
{
    public string Rua { get; set; }
    public string Cidade { get; set; }
}

public class Pessoa
{
    public string Nome { get; set; }
    public Endereco Endereco { get; set; }
}
------------------------

### 132. O que são Delegates?
Delegates são tipos que representam referências a métodos com uma assinatura específica. Eles permitem tratar métodos como objetos e passar métodos como parâmetros para outros métodos.
------------------------
public delegate void MeuDelegate(string mensagem);

public class ExemploDelegate
{
    public void MetodoComDelegate(MeuDelegate meuDelegate)
    {
        meuDelegate("Olá, mundo!");
    }
}
------------------------

### 133. O que são events?
Events (eventos) são membros de uma classe que permitem que a classe ou objeto notifique outras classes ou objetos quando algo acontece. Eventos são baseados em delegates e são usados para implementar o padrão observador.
------------------------
public class Publicador
{
    public event EventHandler MeuEvento;

    protected virtual void OnMeuEvento()
    {
        MeuEvento?.Invoke(this, EventArgs.Empty);
    }

    public void DispararEvento()
    {
        OnMeuEvento();
    }
}
------------------------

### 134. Qual a diferença entre Events e Delegates?
- **Delegates**: São ponteiros de métodos que podem referenciar um ou mais métodos com uma assinatura específica. Eles podem ser invocados diretamente.
- **Events**: São uma forma segura de expor delegates. Eles fornecem um mecanismo para notificação de eventos, permitindo que as classes que disparam eventos não sejam diretamente manipuladas pelos assinantes. Eventos só podem ser invocados dentro da classe onde são declarados.

### 135. O que são os generics?
Generics permitem que classes, interfaces e métodos operem em tipos especificados pelo cliente do código sem comprometer a segurança de tipos. Eles permitem a criação de componentes reutilizáveis que podem trabalhar com qualquer tipo de dado.
------------------------
public class ListaGenerica<T>
{
    private T[] elementos;
    public void Adicionar(T elemento) { }
}
------------------------

### 136. Como restringimos um tipo genérico?
Restringimos um tipo genérico usando constraints, que especificam os requisitos que um tipo deve satisfazer para ser usado como argumento de tipo. Exemplos de constraints incluem `where T : class`, `where T : struct`, e `where T : new()`.
------------------------
public class MinhaClasseGenerica<T> where T : class
{
    private T elemento;
    public void SetElemento(T elemento) { this.elemento = elemento; }
}
------------------------

### 137. Como tratamos erros no C#?
Tratamos erros no C# usando blocos `try-catch-finally`. O bloco `try` contém o código que pode lançar exceções, o bloco `catch` trata as exceções, e o bloco `finally` contém código que deve ser executado independentemente de uma exceção ser lançada ou não.
------------------------
try
{
    // Código que pode lançar exceções
}
catch (Exception ex)
{
    // Código para tratar a exceção
}
finally
{
    // Código que sempre será executado
}
------------------------

### 138. Qual a finalidade do finally?
O bloco `finally` é usado para executar código que deve ser executado independentemente de uma exceção ser lançada ou não. Ele é geralmente usado para liberar recursos ou realizar outras tarefas de limpeza.
------------------------
try
{
    // Código que pode lançar exceções
}
catch (Exception ex)
{
    // Código para tratar a exceção
}
finally
{
    // Código que sempre será executado
}
------------------------

### 139. Para que serve o Try/Parse?
O método `TryParse` é usado para converter strings em tipos de dados numéricos ou de data/hora, retornando um valor booleano que indica se a conversão foi bem-sucedida, sem lançar exceções em caso de falha.
------------------------
int numero;
bool sucesso = int.TryParse("123", out numero);
------------------------

### 140. O que são Tasks?
Tasks são representações assíncronas de unidades de trabalho que podem ser executadas em paralelo. Elas são usadas para operações assíncronas e multithreading.
------------------------
Task minhaTask = Task.Run(() => 
{
    // Código para executar
});
await minhaTask;
------------------------

### 141. Para que serve async/await?
`async` e `await` são usados para simplificar a programação assíncrona. O modificador `async` indica que um método contém código assíncrono, enquanto `await` é usado para pausar a execução de um método assíncrono até que uma `Task` seja concluída.
------------------------
public async Task MeuMetodoAsync()
{
    await Task.Delay(1000);
    Console.WriteLine("Feito");
}
------------------------

### 142. Qual a diferença entre Task.FromResult e o uso de await?
- **Task.FromResult**: Cria uma `Task` que é concluída imediatamente com um resultado especificado. É útil para criar métodos assíncronos que retornam resultados imediatamente.
------------------------
Task<int> resultado = Task.FromResult(42);
------------------------
- **await**: Pausa a execução do método assíncrono até que a `Task` seja concluída, permitindo que o método continue a execução de forma assíncrona.
------------------------
await Task.Delay(1000);
------------------------

### 143. Para que usamos a interface IEquatable?
A interface `IEquatable<T>` é usada para definir um método de comparação específica para um tipo. Implementar `IEquatable<T>` permite comparar objetos de maneira mais eficiente e é especialmente útil em coleções genéricas.
------------------------
public class Pessoa : IEquatable<Pessoa>
{
    public string Nome { get; set; }
    public bool Equals(Pessoa outra)
    {
        return this.Nome == outra.Nome;
    }
}
------------------------

### 144. Para que usamos a interface IComparable?
A interface `IComparable<T>` é usada para definir uma ordem natural de comparação para um tipo. Implementar `IComparable<T>` permite usar objetos desse tipo em operações de ordenação.
------------------------
public class Pessoa : IComparable<Pessoa>
{
    public string Nome { get; set; }
    public int CompareTo(Pessoa outra)
    {
        return this.Nome.CompareTo(outra.Nome);
    }
}
------------------------

### 145. Quando utilizamos a interface IDisposable?
Utilizamos a interface `IDisposable` para liberar recursos não gerenciados, como arquivos, conexões de rede e conexões de banco de dados. Implementar `IDisposable` garante que esses recursos sejam liberados de forma determinística.
------------------------
public class Recurso : IDisposable
{
    public void Dispose()
    {
        // Liberar recursos
    }
}
------------------------

### 146. O que são Extension methods?
Extension methods são métodos que permitem adicionar novas funcionalidades a tipos existentes sem modificar a definição original do tipo. São definidos em métodos estáticos e são chamados como se fossem métodos de instância.
------------------------
public static class MetodosDeExtensao
{
    public static void MeuMetodoDeExtensao(this string str)
    {
        Console.WriteLine(str);
    }
}

// Uso
"Olá, mundo!".MeuMetodoDeExtensao();
------------------------
