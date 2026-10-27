# Design Patterns em Java

Repositório de estudos sobre **Design Patterns** (Padrões de Projeto), com explicações e implementações em Java.

---

## 📖 O que são Design Patterns?

São **soluções reutilizáveis para problemas recorrentes** no design de software orientado a objetos. 
Eles não são código pronto para copiar e colar, mas sim **modelos de solução**: descrevem um problema, o contexto em que ele aparece e uma forma consolidada de resolvê-lo.


### Princípios por trás dos padrões

- Programe para uma **interface**, não para uma implementação.
- Prefira **composição** a herança.
- Encapsule o que **varia**.
- Os padrões andam juntos com os princípios **SOLID**.

> ⚠️ Padrão não é objetivo, é ferramenta. Aplicar pattern onde não há problema só adiciona complexidade.

---

## 🗂️ Categorias

| Categoria | Foco | Quantidade (GoF) |
|---|---|---|
| **Criacionais** | Como os objetos são **criados** | 5 |
| **Estruturais** | Como classes e objetos são **compostos** | 7 |
| **Comportamentais** | Como objetos **interagem** e dividem responsabilidades | 11 |

---

## 🏗️ Padrões Criacionais

Abstraem o processo de instanciação, deixando o sistema independente de como seus objetos são criados.

| Padrão | Ideia central | Exemplo no Java/Spring |
|---|---|---|
| **Singleton** | Garante uma única instância de uma classe com acesso global a ela. | `Runtime.getRuntime()`, beans Spring (escopo padrão) |
| **Factory Method** | Define um método para criar objetos, deixando as subclasses decidirem qual classe instanciar. | `Calendar.getInstance()` |
| **Abstract Factory** | Cria famílias de objetos relacionados sem especificar as classes concretas. | `DocumentBuilderFactory` |
| **Builder** | Constrói objetos complexos passo a passo, separando construção de representação. | `StringBuilder`, `HttpClient.newBuilder()`, `@Builder` do Lombok |
| **Prototype** | Cria novos objetos copiando (clonando) uma instância existente. | `Object.clone()` |

---

## 🧱 Padrões Estruturais

Tratam de como classes e objetos se combinam para formar estruturas maiores.

| Padrão | Ideia central | Exemplo no Java/Spring |
|---|---|---|
| **Adapter** | Converte a interface de uma classe em outra que o cliente espera. | `Arrays.asList()`, `InputStreamReader` |
| **Bridge** | Separa uma abstração da sua implementação para que ambas variem independentemente. | JDBC (`DriverManager` + drivers) |
| **Composite** | Compõe objetos em árvore e trata objetos individuais e composições da mesma forma. | `java.awt.Container` |
| **Decorator** | Adiciona responsabilidades a um objeto dinamicamente, sem alterar sua classe. | `BufferedInputStream`, `Collections.unmodifiableList()` |
| **Facade** | Oferece uma interface simplificada para um subsistema complexo. | `JdbcTemplate` do Spring |
| **Flyweight** | Compartilha objetos para economizar memória quando há muitas instâncias parecidas. | `Integer.valueOf()` (cache de -128 a 127) |
| **Proxy** | Fornece um substituto que controla o acesso a outro objeto. | `java.lang.reflect.Proxy`, Spring AOP, lazy loading do Hibernate |

---

## 🔄 Padrões Comportamentais

Tratam de algoritmos e da distribuição de responsabilidades entre objetos.

| Padrão | Ideia central | Exemplo no Java/Spring |
|---|---|---|
| **Chain of Responsibility** | Passa uma requisição por uma cadeia de handlers até que um deles a trate. | `Filter` / `FilterChain` (Servlets), Spring Security |
| **Command** | Encapsula uma requisição como objeto (permite fila, log, desfazer). | `Runnable` |
| **Interpreter** | Define uma gramática e um interpretador para uma linguagem. | `java.util.regex.Pattern` |
| **Iterator** | Percorre os elementos de uma coleção sem expor sua estrutura interna. | `java.util.Iterator` |
| **Mediator** | Centraliza a comunicação entre objetos, reduzindo dependências diretas entre eles. | `DispatcherServlet` do Spring MVC |
| **Memento** | Captura e restaura o estado de um objeto sem violar o encapsulamento. | Funcionalidade de "desfazer" em editores |
| **Observer** | Quando um objeto muda de estado, seus dependentes são notificados. | `PropertyChangeListener`, `ApplicationEventPublisher` do Spring |
| **State** | Muda o comportamento de um objeto conforme seu estado interno. | Máquina de estados de um pedido (criado → pago → enviado) |
| **Strategy** | Define uma família de algoritmos intercambiáveis em tempo de execução. | `Comparator` |
| **Template Method** | Define o esqueleto de um algoritmo e deixa subclasses implementarem etapas específicas. | `AbstractList`, `JdbcTemplate` |
| **Visitor** | Adiciona novas operações a uma estrutura de objetos sem modificá-la. | `FileVisitor` (`Files.walkFileTree`) |

---

## 📁 Estrutura do repositório

```
design-patterns/
├── creational/
│   ├── singleton/
│   ├── factory-method/
│   ├── abstract-factory/
│   ├── builder/
│   └── prototype/
├── structural/
│   ├── adapter/
│   ├── bridge/
│   ├── composite/
│   ├── decorator/
│   ├── facade/
│   ├── flyweight/
│   └── proxy/
└── behavioral/
    ├── chain-of-responsibility/
    ├── command/
    ├── interpreter/
    ├── iterator/
    ├── mediator/
    ├── memento/
    ├── observer/
    ├── state/
    ├── strategy/
    ├── template-method/
    └── visitor/
```

Cada pasta traz:
- um `README.md` com o problema, a solução e o diagrama;
- a implementação em Java;
- testes demonstrando o uso.

---

## ✅ Progresso

### Criacionais
- [ ] Singleton
- [ ] Factory Method
- [ ] Abstract Factory
- [ ] Builder
- [ ] Prototype

### Estruturais
- [ ] Adapter
- [ ] Bridge
- [ ] Composite
- [ ] Decorator
- [ ] Facade
- [ ] Flyweight
- [ ] Proxy

### Comportamentais
- [ ] Chain of Responsibility
- [ ] Command
- [ ] Interpreter
- [ ] Iterator
- [ ] Mediator
- [ ] Memento
- [ ] Observer
- [ ] State
- [ ] Strategy
- [ ] Template Method
- [ ] Visitor

---

## 🛠️ Tecnologias

- Java 21
- Maven
- JUnit 5

---

## 📚 Referências

- GAMMA, E.; HELM, R.; JOHNSON, R.; VLISSIDES, J. *Design Patterns: Elements of Reusable Object-Oriented Software*. Addison-Wesley, 1994.
- FREEMAN, E.; ROBSON, E. *Head First Design Patterns*. O'Reilly.
- [Refactoring.Guru – Design Patterns](https://refactoring.guru/pt-br/design-patterns)
