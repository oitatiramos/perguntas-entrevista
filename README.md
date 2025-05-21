
# Guia de Perguntas para Entrevista de Programador Java

🚩 **Atenção:**  
Para se sair bem numa entrevista, não basta decorar respostas. É muito importante entender **os conceitos por trás** de cada pergunta. Ter exemplos práticos na cabeça ajuda muito a explicar melhor e impressionar o entrevistador.  

---

## 1. O que é a JVM, JDK e JRE?

- **JVM (Java Virtual Machine):** É a máquina virtual que executa o código Java, interpretando o bytecode e garantindo que o programa rode em qualquer sistema.  
- **JDK (Java Development Kit):** É o kit completo para desenvolver Java, inclui compilador, ferramentas e a JVM.  
- **JRE (Java Runtime Environment):** É o ambiente de execução, contém a JVM e bibliotecas para rodar a aplicação, mas não tem ferramentas de desenvolvimento.

**Exemplo:**  
```java
// Código Java compilado em bytecode é executado pela JVM
public class OlaMundo {
    public static void main(String[] args) {
        System.out.println("Olá, mundo!");
    }
}
```

---

## 2. Qual a diferença entre `==` e `.equals()`?

- `==` compara se dois objetos são o **mesmo na memória** (referência).  
- `.equals()` compara o **conteúdo** dos objetos, se implementado.

**Exemplo:**  
```java
String a = new String("teste");
String b = new String("teste");

System.out.println(a == b);       // false (objetos diferentes)
System.out.println(a.equals(b));  // true  (conteúdo igual)
```

---

## 3. O que são classes abstratas e interfaces?

- **Classe abstrata:** Pode ter métodos implementados e abstratos (sem implementação), serve como base para outras classes.  
- **Interface:** Define métodos que uma classe deve implementar, é um contrato, geralmente sem implementação.

**Exemplo:**  
```java
abstract class Animal {
    abstract void fazerSom();
    void dormir() {
        System.out.println("Dormindo...");
    }
}

interface Voar {
    void voar();
}
```

---

## 4. O que é encapsulamento?

Esconder os dados internos da classe e controlar o acesso por meio de métodos `get` e `set`. Isso protege o objeto e organiza o código.

**Exemplo:**  
```java
public class Pessoa {
    private String nome;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }
}
```

---

## 5. O que é herança?

Quando uma classe herda atributos e métodos de outra, permitindo reutilizar código.

**Exemplo:**  
```java
class Animal {
    void comer() {
        System.out.println("Comendo...");
    }
}

class Cachorro extends Animal {
    void latir() {
        System.out.println("Au au!");
    }
}
```

---

## 6. Como funciona o tratamento de exceções?

Usamos `try`, `catch`, `finally` para tratar erros e evitar que o programa pare abruptamente.

**Exemplo:**  
```java
try {
    int[] nums = {1, 2};
    System.out.println(nums[5]);
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Índice inválido!");
}
```

---

## 7. O que é uma `List`, `Set` e `Map`?

- **List:** Lista ordenada que aceita elementos duplicados.  
- **Set:** Conjunto que não aceita elementos duplicados.  
- **Map:** Estrutura de chave-valor.

**Exemplo:**  
```java
List<String> lista = new ArrayList<>();
Set<String> conjunto = new HashSet<>();
Map<String, String> mapa = new HashMap<>();
```

---

## 8. O que é o Spring Boot?

Framework que facilita a criação de aplicações Java, principalmente APIs, com configuração mínima.

---

## 9. O que são beans no Spring?

Objetos gerenciados pelo Spring, que cuida da criação, configuração e ciclo de vida deles.

---

## 10. Como funciona a injeção de dependência?

Spring cria e injeta objetos automaticamente para deixar o código mais limpo e testável.

**Exemplo:**  
```java
@Component
public class Servico {}

@RestController
public class Controlador {
    @Autowired
    private Servico servico;
}
```

---

# Perguntas da Simulação com Exemplos

---

### O que é a JVM e qual o papel dela?

A JVM executa o bytecode Java, tornando o código independente de plataforma.

---

### Qual a diferença entre `ArrayList` e `LinkedList`?

- `ArrayList` é baseado em array, rápido para acessar elementos, lento para inserir/remover no meio.  
- `LinkedList` é uma lista encadeada, rápido para inserir/remover, mais lento para acesso direto.

---

### O que é o `final` em Java?

- Em variável: valor fixo, não pode mudar.  
- Em método: não pode ser sobrescrito.  
- Em classe: não pode ser estendida.

---

### O que são exceções checked e unchecked?

- Checked: o compilador exige tratamento.  
- Unchecked: não é obrigatório tratar, geralmente erros de programação.

---

### O que é Spring Boot e por que usar?

Facilita o desenvolvimento rápido de APIs Java, com configurações automáticas.

---

### O que é uma interface em Java?

Um contrato que define métodos que a classe deve implementar.

---

### O que é `@Autowired`?

Anotação do Spring para injetar dependências automaticamente.

---

# Dica final

Para cada conceito, tente **entender o porquê** e usar **exemplos simples** ao explicar. Isso mostra domínio e facilita o entendimento do entrevistador.
