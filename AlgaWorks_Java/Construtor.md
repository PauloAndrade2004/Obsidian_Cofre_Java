## Construtor Vazio

Em Java, o construtor vazio é (também conhecido de construtor padrão) é um tipo de construtor que não recebe nenhum argumento.

* Usamos quando queremos criar Objetos de uma classe , é não queremos passar parâmetro no momento da criação.
		<font color="#92cddc">Podemos sitar como exemplo o titular1 que criamos, nele definimos os atributos individualmente, aonde utilizamos os métodos</font> <font color="#ff0000">set</font> <font color="#92cddc">para atribuir valores á instância</font>.

Exemplo : 
```Java 
public class Principal {  
  
    public static void main(String[] args) {  
        // criando a Pessoa titular1.  
        Pessoa titular1 = new Pessoa();  
        titular1.setNome("Gabrielle");  
        titular1.setDocumento("5006361847");  

        contaTitular1.setTitular(titular1);  
        contaTitular1.setAgencia(555);  
        contaTitular1.setNumero(123);  
        contaTitular1.setSaldo(500); // Titular 1 inicia com um saldo de R$ 500,00.
```

## Construtor com parâmetros

Construtor com parâmetros permite que você crie uma <font color="#b7dde8">instância</font> de <font color="#b7dde8">Conta</font> utilizando todos os <font color="#b7dde8">valores necessários passador diretamente no momento que criamos o Objeto</font>. <font color="#b7dde8">Adicionamos</font> ele dentro dos <font color="#b7dde8">parênteses</font>. 

Muito utilizado quando já temos os dados necessários do para inicializar o objeto de uma maneira mais compacta e eficiente.

```Java
Pessoa titular2 = new Pessoa();  
titular2.setNome("Paulo");  
titular2.setDocumento("5006361847");  
  
Conta contaTitular2 = new Conta(titular2, 555, 124, 1000); 
```


### Atenção 

* O <font color="#92cddc">titular2</font> está sendo passado como <font color="#ff0000">parâmetro</font> para o construtor de Conta. 
*  O <font color="#92cddc">titular2</font> é um objeto da classe Pessoa que representa o titular da conta. Ou seja, está ocorrendo a <font color="#ff0000">associação</font> do <font color="#92cddc">titular2</font> com a <font color="#92cddc">Conta</font>.
* Esse tipo de associação entre objetos deixa claro que **a conta está associada a um titular específico**, e as informações da conta (como agência, número e saldo) pertencem diretamente a esse titular. Portanto, a conta de "Paulo" (o titular2) tem esses dados que você passou no momento da criação