# SOLID
SOLID é um acrônimo que representa cinco princípios da programação orientada a objetos, introduzidos por Robert C. Martin (também conhecido como Uncle Bob). Esses princípios ajudam a criar sistemas de software que são mais fáceis de entender, manter e expandir. Aqui está o que cada letra do acrônimo significa:

### S - Single Responsibility Principle (Princípio da Responsabilidade Única)
Uma classe deve ter apenas uma única responsabilidade ou razão para mudar. Isso significa que cada classe deve encapsular apenas uma parte do funcionamento do sistema, evitando que ela tenha múltiplas responsabilidades.

Exemplo prático, imagine uma classe que cadastra usuários e envia email de boas vindas aplicando esse princípio.
```shell
class CadastrarUsuario
{
	# Utilizando o Contructor Property Promotion

	public function __constructor(public string $nome, public strinc $email){}
}

# agora criar uma classe responsavel por enviar o email
class Mail
{
	public function send(string $nome, string $email): void
	{
		// aqui a lógica para envio do email
		echo "==============";
		echo "Email enviado com sucesso!";
		echo "==============";

	}

	public fuction validar_email(string $email): bool
	{
		return (bool) filter_var($email, FILTER_VALIDATE_EMAIL);
	}
}
```

### O - Open/Closed Principle (Princípio Aberto/Fechado)
   - As entidades de software (classes, módulos, funções, etc.) devem estar abertas para extensão, mas fechadas para modificação. Isso significa que o comportamento de uma classe pode ser estendido sem alterar seu código-fonte existente.



### L - Liskov Substitution Principle (Princípio da Substituição de Liskov)
   - Subtipos devem ser substituíveis por seus tipos base sem alterar a corretude do programa. Em outras palavras, os objetos de uma classe derivada devem poder substituir os objetos da classe base sem que o comportamento do programa seja alterado.



### I - Interface Segregation Principle (Princípio da Segregação de Interfaces)
   - Uma classe não deve ser forçada a implementar interfaces que não utiliza. Em vez de criar interfaces grandes e complexas, é melhor criar várias interfaces menores e mais específicas, cada uma adequada a um conjunto de clientes.



### D - Dependency Inversion Principle (Princípio da Inversão de Dependência)
   - Módulos de alto nível não devem depender de módulos de baixo nível. Ambos devem depender de abstrações. Além disso, abstrações não devem depender de detalhes; detalhes devem depender de abstrações. Isso promove a flexibilidade e a reutilização do código.




Esses princípios são fundamentais para o desenvolvimento de software orientado a objetos e ajudam a garantir que o código seja mais modular, fácil de testar e menos propenso a erros e dificuldades de manutenção.