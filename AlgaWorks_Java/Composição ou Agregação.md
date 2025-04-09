Em Java, podemos dizer que quando estanciamos uma classe dentro de outra com um atributo, você está realizando #composição ou seja, a classe "<font color="#92cddc">"tem"</font> outra classe que faz parte dela.

Exemplo : 

Classe Pessoa : 
```Java 
public class Pessoa {  
  
    private String nome;  
    private String documento;  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public String getDocumento() {  
        return documento;  
    }  
  
    public void setDocumento(String documento) {  
        this.documento = documento;  
    }  
}
```


Classe <font color="#92cddc">Conta</font> : 
```Java 
import java.util.Objects;  
  
public class Conta {  
  
        private Pessoa titular;  
        private int agencia;  
        private int numero;  
        private double saldo;  
  
        // Getters e Setters  
  
    public int getAgencia() {  
        return agencia;  
    }  
    public void setAgencia(int agencia) {  
        this.agencia = agencia;  
    }  
  
    public int getNumero() {  
        return numero;  
    }  
    public void setNumero(int numero) {  
        this.numero = numero;  
    }  
    public double getSaldo() {  
        return saldo;  
    }  
    public void setSaldo(double saldo) {  
        this.saldo = saldo;  
    }  
  
        //Adicionando construtor  
  
        //como implementar um metodo na classe?    public void depositarDinhero(double valor /*Variavel local (valor) */) {  
        saldo += valor;  
        System.out.println("Deposito realizado no valor de: " + valor);  
    }  

}
```

* Neste caso, o atributo titular é uma instância da classe Pessoa que se encontra dentro da classe Conta.

* A composição indica que a existência de uma uma conta esta intimamente ligadas a uma Pessoa.

* Utilizamos quando queremos modelar relacionamentos entre classes de forma mais realista e Organizada.

## Relacionamento Natural
Ocorre quando queremos modelar um relacionamento. Podemos citar como exemplo, uma classe <span style="background:#b1ffff">Conta</span> tem uma Pessoa (<span style="background:#b1ffff">titular</span>). Ou seja, <span style="background:#b1ffff">Cada Conta precisa ter um titular, para que ela seja válida precisa ter alguma Pessoa associada.</span>


## Evitar Herança Desnecessária

A composição é uma alternativa importante á herança quando não queremos a utiliza-la. 

Exemplo: 

Podemos ter uma classe Pessoa e outra classe Cliente, não faria muito sentido nós herdarmos a classe Pessoa. <font color="#b7dde8">Com isso classe Pessoa tem características e comportamentos adicionais</font>. A <font color="#b7dde8">composição</font> permite que o cliente tenha uma <font color="#b7dde8">Pessoa</font> com atributo, sem a complexidade da herança.