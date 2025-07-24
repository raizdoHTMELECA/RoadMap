# Anotações sobre encapsulamentos;

### O Que São Métodos Get e Set?

- **Métodos `get` (Acessores):** São usados para **obter** ou **ler** o valor de um atributo (variável) de um objeto. No seu exemplo, `getTesteName()` é usado para recuperar o nome que foi armazenado no objeto `novaPessoa`.
- **Métodos `set` (Modificadores):** São usados para **definir** ou **modificar** o valor de um atributo de um objeto. Em seu código, `setTesteName(sc.next())` está definindo o nome do objeto `novaPessoa` com o valor que o usuário digita no console

### O Sentido de Usar Getters e Setters: Encapsulamento

O principal objetivo de usar `get` e `set` é proteger os dados de um objeto de acessos e modificações diretas e indesejadas. Isso é o que chamamos de **encapsulamento**.

### No seu Contexto

```java
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        var novaPessoa = new Teste();
        novaPessoa.setTesteName(sc.next());
        System.out.printf("A pessoa se chama: %s", novaPessoa.getTesteName());

    }
}
```

No seu código:

1. `var novaPessoa = new Teste();` cria um objeto da classe `Teste`.
2. `novaPessoa.setTesteName(sc.next());` utiliza o método `set` para pegar a entrada do usuário (`sc.next()`) e **guardar de forma segura e controlada** dentro do objeto `novaPessoa`.
3. `System.out.println(novaPessoa.getTesteName());` utiliza o método `get` para **acessar de forma segura** o nome que foi guardado e exibi-lo.

Em resumo, `get` e `set` não são ferramentas, mas sim **métodos que implementam o princípio do encapsulamento**. Eles são a maneira padrão e correta em Java e em muitas outras linguagens orientadas a objetos de proteger e manipular os dados de um objeto, garantindo maior segurança, flexibilidade e controle sobre o seu código.