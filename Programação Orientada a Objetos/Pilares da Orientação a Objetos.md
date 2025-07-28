# **Resumo da Seção 9: Pilares da Orientação a Objetos**

Esta sessão aborda conceitos fundamentais na Programação Orientada a Objetos (POO) que permitem a criação de classes mais robustas, flexíveis e seguras.

#### **1. Construtores**

- **O que são?** São "métodos especiais" responsáveis por criar e inicializar um objeto no momento em que ele é instanciado. O construtor define o estado inicial do objeto.

- **Características Principais:**

  - Têm o **mesmo nome** da classe.
  - **Não possuem tipo de retorno**, nem mesmo `void`.
  - São chamados automaticamente com o operador `new`.

- **Exemplo Básico (Java/C#):**

  Java

  ```
  public class Produto {
      public String nome;
  
      // Construtor
      public Produto(String nomeInicial) {
          this.nome = nomeInicial;
      }
  }
  
  // Uso:
  Produto p = new Produto("Caneta"); // O construtor é chamado aqui
  ```

#### **2. Palavra `this`**

- **O que é?** É uma referência para o **próprio objeto** atual. Dentro de um método ou construtor, `this` se refere à instância que o chamou.

- **Usos Comuns:**

  1. **Desambiguação:** Diferenciar atributos de variáveis locais (ou parâmetros) quando eles têm o mesmo nome.

     Java

     ```
     public void setNome(String nome) {
         this.nome = nome; // this.nome (atributo) recebe o valor do parâmetro nome
     }
     ```

  2. **Chamar Construtores:** Usar `this()` para chamar outro construtor da mesma classe (útil em sobrecarga de construtores).

#### **3. Sobrecarga (Overloading)**

- **O que é?** É a capacidade de definir **vários métodos com o mesmo nome** na mesma classe, desde que suas **assinaturas sejam diferentes**.

- **O que torna a assinatura diferente?**

  - O **número** de parâmetros.
  - O **tipo** dos parâmetros.
  - A **ordem** dos tipos dos parâmetros.

- **Importante:** O tipo de retorno **não** faz parte da assinatura para fins de sobrecarga.

- **Exemplo (Java/C#):**

  Java

  ```java
  public class Calculadora {
      public int somar(int a, int b) {
          return a + b;
      }
  
      // Sobrecarga com três parâmetros
      public int somar(int a, int b, int c) {
          return a + b + c;
      }
  
      // Sobrecarga com tipos diferentes
      public double somar(double a, double b) {
          return a + b;
      }
  }
  ```



#### **4. Encapsulamento**

- **O que é?** É o princípio de **"esconder" os detalhes de implementação** de um objeto, expondo apenas uma interface pública e segura para interagir com ele. O objetivo é proteger a integridade dos dados do objeto.

- **Como é implementado?**

  1. **Atributos Privados:** Os atributos (variáveis) da classe são declarados como `private` para que não possam ser acessados diretamente de fora da classe.
  2. **Métodos Públicos (Getters e Setters):** São criados métodos `public` para ler (`get`) e modificar (`set`) os atributos privados. Isso permite adicionar lógica e validação antes de alterar o estado do objeto.

- **Vantagens:**

  - **Controle:** A classe tem controle total sobre seus dados.
  - **Segurança:** Impede que dados sejam corrompidos com valores inválidos.
  - **Flexibilidade:** A implementação interna pode ser alterada sem impactar o código que utiliza a classe.

- **Exemplo (Java/C#):**

  Java

  ```java
  public class ContaBancaria {
      private double saldo; // Atributo privado
  
      // Getter: método público para ler o saldo
      public double getSaldo() {
          return this.saldo;
      }
  
      // Setter: método público para modificar o saldo com validação
      public void depositar(double valor) {
          if (valor > 0) {
              this.saldo += valor;
          }
      }
  }
  ```