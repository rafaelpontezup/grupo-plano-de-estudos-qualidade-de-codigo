# Plano de estudos sobre Design e Qualidade de Código

Se 80% do que você faz no dia a dia como desenvolvedor(a) é ler e escrever código, então nada mais justo do que investir no seu aprendizado sobre como desenhar e escrever código de qualidade. Neste plano de estudos vamos navegar por diversos conceitos, técnicas, dicas de design e tradeoffs ao escrever código que seja fácil de ler e entender, simples de manter a médio-longo prazo e flexível o suficiente para ser evoluído mitigando a complexidade acidental.

Para isso, vamos estudar orientação a objetos, técnicas e conceitos de programação pragmática, design patterns e alguns estilos arquiteturais para organizar e estruturar nosso código. Focaremos na linguagem Java, mas boa parte do que veremos são conceitos do paradigma orientado a objetos que podem ser facilmente aplicados com outras linguagens e plataformas.

Aqui assumimos que você já possui algum conhecimento sobre os temas abordados ou já os pratica no dia a dia, pois dessa forma podemos ir mais longe e abrir sua mente sobre as ferramentas que você tem em mãos mas provavelmente não está tirando máximo proveito. Abaixo os tópicos principais que estudaremos:

1. [Orientação a objetos e técnicas de design de código](#1-orienta%C3%A7%C3%A3o-a-objetos-e-t%C3%A9cnicas-de-design-de-c%C3%B3digo)
2. [Revisitando Design Patterns](#2-revisitando-design-patterns)
3. [SOLID: ou como juntar OO e design patterns na mesma panela](#3-solid-ou-como-juntar-oo-e-design-patterns-na-mesma-panela)
4. [Design e arquitetura de código](#4-design-e-arquitetura-de-código)

Ao fim desse plano de estudos, você terá heuristicas úteis que te ajudarão a olhar para trechos de código e que te permitirão identificar oportunidades de refatoração e implementação de código com maior qualidade e que também elevará regua em sessões de code review.

## 1. Orientação a objetos e técnicas de design de código

Por algum motivo nos convenceram que orientação a objetos é algo simples, mas a verdade é que não é. Ao estudar sobre o conteúdo que curamos aqui você vai entender que o **cerne da OO se baseia em manter estado e comportamentos juntos**. Quanto mais cedo você entender isso mais facilmente você saberá como encapsulamento, polimorfismo e composição se encaixam no seu design.

Junto a OO, também estudaremos algumas técnicas que irão te guiar no dia a dia para escrever código mais enxuto, fléxivel e de fácil manutenção. E, por fim, você também vai aprender como especialistas usam todos estes conceitos e técnicas no dia a dia através de heurísticas que vão te colocar noutro patamar na hora de escrever, refatorar e revisar código.

### 1.1. Conteúdo teórico

1. Orientação a Objetos
    - 1.1. [Introdução: Programação Orientada a Objetos e programação estruturada](https://www.alura.com.br/artigos/poo-programacao-orientada-a-objetos) (10min)
    - 1.2. [Objetos não são atributos + funções 🤯](https://web.archive.org/web/20150605222727/http://blog.fragmental.com.br/2008/05/18/objetos-nao-sao-atributos-funcoes/trackback/index.html) (7min)
    - 1.3. [Como não aprender Java e Orientação a Objetos: getters e setters](https://www.alura.com.br/artigos/nao-aprender-oo-getters-e-setters) (10min)
    - 1.4. [Como não aprender orientação a objetos: Herança](https://www.alura.com.br/artigos/como-nao-aprender-orientacao-a-objetos-heranca) (12min)
    - 1.5. [Como não aprender orientação a objetos: o excesso de ifs](https://www.alura.com.br/artigos/como-nao-aprender-orientacao-a-objetos-o-excesso-de-ifs) (10min)
    - 1.6. [Fantoches](https://web.archive.org/web/20140713021108/http://fragmental.com.br/wiki/index.php/Fantoches.html) (8min)
    - 1.7. [Evitando VOs e BOs](https://web.archive.org/web/20140707091808/http://fragmental.com.br/wiki/index.php/Evitando_VOs_e_BOs.html) (7min)
    - 1.8. [Enums são mais que constantes 🤯](http://blog.triadworks.com.br/enums-sao-mais-que-constantes) (6min)
    - 1.9. [OO na Prática: representando o usuário logado no sistema](http://blog.triadworks.com.br/oo-na-pratica-representando-o-usuario-logado-no-sistema) (8min)
    - 1.10. [OO na Prática: Cuidados com relacionamento bidirecional](http://blog.triadworks.com.br/jpa-por-que-voce-deveria-evitar-relacionamento-bidirecional) (10min)
    - 1.11. [OO na Prática: Controle Transacional Programático em Sistemas Legados](http://blog.triadworks.com.br/controle-transacional-programatico-em-sistemas-legados) (15min)
    - 1.12. [OO na Prática: Evite condicionais em JavaScript com o uso de Duck Typing](http://blog.triadworks.com.br/evite-condicionais-em-javascript-com-o-uso-de-duck-typing) (8min)
2. Tell, don’t ask e The Law of Demeter
    - 2.1. [Tell, Don't Ask](https://web.archive.org/web/20071028192420/https://pragprog.com/articles/tell-dont-ask) (10min)
    - 2.2. [TellDontAsk - What Martin Fowler thinks about it?](https://martinfowler.com/bliki/TellDontAsk.html) (8min)
    - 2.3. [Tell, Don't Ask, The Pragmatic Way](https://programmingwithmosh.com/net/tell-dont-ask-the-pragmatic-way/) (12min)
    - 2.4. [Tell, don’t ask (by Robson Castilho)](https://robsoncastilho.com.br/2014/05/11/conceitos-tell-dont-ask/) (10min)
    - 2.5. [The Law of Demeter - Writing Shy Code](https://codeahoy.com/2016/06/17/the-law-of-demeter-writing-shy-code/) (10min)
    - 2.5. [Java examples of the Law of Demeter](https://alvinalexander.com/java/java-law-of-demeter-java-examples/) (10min)
3. Early Return e Fail Fast
    - 3.1. [Return Early Pattern](https://medium.com/swlh/return-early-pattern-3d18a41bba8) (7min)
    - 3.2. [Fail Fast (2004)](https://www.martinfowler.com/ieeeSoftware/failFast.pdf) (15min)
    - 3.3. [How to Make Readable Code: Return Early or If Statement?](https://methodpoet.com/return-early-or-if-statement/) (8min)
    - 3.4. [Are Early Returns Any Good?](https://betterprogramming.pub/are-early-returns-any-good-eed4b4d03866) (10min) 
4. Design by Contract
    - 4.1. [Contratos Nulos 🤯](https://web.archive.org/web/20100612013930/http://fragmental.com.br/wiki/index.php/Contratos_Nulos) (8min)
    - 4.2. [Wikipedia: Design by contract](https://en.wikipedia.org/wiki/Design_by_contract) (15min)
    - 4.3. [Assertion and Design by Contract in Java](https://www.section.io/engineering-education/assertion-and-design-by-contract-in-java/) (12min)
    - 4.4. [Programming by contract on the JVM](https://blog.frankel.ch/programming-by-contract-jvm/) (10min)
    - 4.5. [3 Benefits of Design by Contract](https://blog.devgenius.io/3-benefits-of-design-by-contract-d5752f3c7468) (7min)
5. Heurísticas de código OO no mundo real 
    - 5.1. [Refatoração: Sete situações que eu percebo de maneira quase automática 🤯](https://www.youtube.com/watch?v=X328oOMy7vk&ab_channel=DevEficiente) (28min)
    - 5.2. [Como evitar um dos piores acoplamentos que existem](https://www.youtube.com/watch?v=PagCAo4Ch1U&t=3s&ab_channel=DevEficiente) (13min)
    - 5.3. [Como eu sei se devo criar ou não uma nova abstração para um determinado parâmetro/retorno?](https://www.youtube.com/watch?v=gBQ7zDzvqyY&t=5s&ab_channel=DevEficiente) (32min)
    - 5.4. [Acoplamento distribuído: O fundo do poço dos acoplamentos](https://www.youtube.com/watch?v=OztU-cxkxn8&t=5s&ab_channel=DevEficiente) (30min)
    - 5.5. [Encapsulamento para ganhar mais coesão: O feijão com arroz que precisa estar dominado](https://www.youtube.com/watch?v=2Bso1Yg3xUA&t=2s&ab_channel=DevEficiente) (22min)


### 1.2. Como posso me avaliar?

Agora que você já se sente mais confortável com OO e as técnicas de design de código discutidas até aqui, vamos validar nosso conhecimento através de atividades práticas 💪🏻

#### **❓Atividade 1**:

Que tal olhar para seu projeto atual e identificar trechos de código com grande potencial de melhoria de qualidade?

É isso mesmo, é hora de refatorar código 🥳🥳

Para cada trecho de código que você identificar no seu projeto, faça:

- a) Se possível, refatore o código do projeto e submeta uma PR para revisão; aproveite e discuta com seu time sobre as motivações do seu refactoring e os pontos positivos que você enxega;
- b) Crie [Gists](https://gist.github.com/) com a versão de antes e depois da refatoração, e por fim compartilhe-os no [nosso forum do Github](https://github.com/rafaelpontezup/grupo-plano-de-estudos-qualidade-de-codigo/discussions) para melhor feedback e discussões; 

>⚠️ **Privacidade e confidencialidade**<br/>
> Lembre-se dos cuidados ao compartilhar código fora da empresa, **crie Gists privados** na sua conta da Zup no Github, evite expor dados sensíveis do seu projeto e compartilhe somente com Zuppers.

#### **❓Atividade 2**:

Por fim, se você ainda não fez nossa avaliação [**Knowledge about Object-Oriented Design**](https://hr.gs/badge-knowledge-about-object-oriented-design) ou se não obteve êxito nela, essa é uma excelente oportunidade para (re)fazê-la.

[Acesse o link da avaliação](https://hr.gs/badge-knowledge-about-object-oriented-design) e valide seus conhecimentos sobre design de código orientado a objetos! 🎯 

## 2. Revisitando Design Patterns

Embora você tenha adicionado diversas heurísticas de código no seu cinto de utilidades, muitos problemas comuns em projetos de software são facilmente identificados e solucinados através de "receitas prontas", conhecidas como Design Patterns (ou Padrões de Projetos, do português). Não à toa, um bom desenvolvedor(a) precisa conhecer os principais design patterns catalogados, quais os tipos de problemas de design de código que eles resolvem e por fim conseguir facilmente aplicá-los.

Esta é uma boa oportunidade para revisitarmos alguns patterns populares e tentar conectá-los com nosso aprendizado sobre design OO 😁

### 2.1. Conteúdo teórico

1. [Design patterns: Breve introdução aos padrões de projeto](https://www.alura.com.br/artigos/design-patterns-introducao-padroes-projeto) (15min)
2. Creational Design Patterns
    - 2.1. [Factory Method](https://refactoring.guru/design-patterns/factory-method) (20min)
    - 2.2. [Builder](https://refactoring.guru/design-patterns/builder) (20min)
    - 2.3. [Singleton](https://refactoring.guru/design-patterns/singleton) (15min)
3. Structural Design Patterns
    - 3.1. [Facade](https://refactoring.guru/design-patterns/facade) (15min)
    - 3.2. [Decorator](https://refactoring.guru/design-patterns/decorator) (20min)
    - 3.3. [Proxy](https://refactoring.guru/design-patterns/proxy) (20min)
4. Behavior Design Patterns
    - 4.1. [Command](https://refactoring.guru/design-patterns/command) (20min)
    - 4.2. [Strategy](https://refactoring.guru/design-patterns/strategy) (20min)
    - 4.3. [Observer](https://refactoring.guru/design-patterns/observer) (20min)
    - 4.4. [Template Method](https://refactoring.guru/design-patterns/template-method) (15min)
5. Inversion of Control (IoC) e Dependency Injection (DI)
    - 5.1. [Inversion of Control Containers and the Dependency Injection pattern](https://www.martinfowler.com/articles/injection.html) (45min)
    - 5.2. [Demystifying Inversion of Control (IoC)](https://dev.to/parasmm/demystifying-inversion-of-control-ioc-3670) (12min)
6. Functional Programming Patterns e Loan Design Pattern
    - 6.1. [Functional Programming Patterns With Java 8](https://dzone.com/articles/functional-programming-patterns-with-java-8) (20min)
    - 6.2. [Loan pattern in Java (a.k.a lender lendee pattern)](https://www.javacodegeeks.com/2013/01/loan-pattern-in-java-a-k-a-lender-lendee-pattern.html) (10min)
    - 6.3. [Exemplo de código usando Loan Pattern para envio de email](https://gist.github.com/rakeshopensource/47ff319aba116de7843b5787fa3ed775) (10min)
    - 6.4. [Usando Loan Pattern para gerenciamento de recursos caros: Transaction Manager](http://blog.triadworks.com.br/controle-transacional-programatico-em-sistemas-legados) (15min)

### 2.2. Como posso me avaliar?

Hora de validar nosso conhecimento sobre design patterns, mas desta vez vamos exercitar nossa habilidade de escrever artigos a fim de ajudar outros desenvolvedores(as) dentro e fora da Zup 💪🏻

#### **❓Atividade 1**:

Escreva um artigo sobre Loan Design Pattern para ajudar seu time a conhecer melhor este padrão de projeto, os tipos de problemas que ele resolve e como identificar oportunidades de aplicá-lo.

>⚠️ **Lembre-se de compartilhar seu artigo**<br/>
> Você pode escrever o artigo onde você achar melhor (como Gist, Google Docs, blog pessoal etc), o importante é que você consiga compartilhá-lo com nossa turma e monitor através de um link público no [nosso forum do Github](https://github.com/rafaelpontezup/grupo-plano-de-estudos-qualidade-de-codigo/discussions) 😊

#### **❓Atividade 2**:

Por fim, se você ainda não fez nossa avaliação [**Knowledge about Design Patterns**](https://hr.gs/badge-knowledge-about-design-patterns) ou se não obteve êxito nela, essa é uma excelente oportunidade para (re)fazê-la.

[Acesse o link da avaliação](https://hr.gs/badge-knowledge-about-design-patterns) e valide seus conhecimentos sobre os principais e mais utilizados design patterns no mercado! 🎯

## 3. SOLID: ou como juntar OO e design patterns na mesma panela

Além dos design patterns que estudamos no tópico anterior, existe um conjunto de 5 principios que foram apresentados por Robert C. Martin (Uncle Bob) há +20 anos atrás para ajudar desenvolvedores(as) a escrever código que seja fácil de entender e fácil de mudar. Mais tarde, estes principios ficaram conhecidos pelo acronimo SOLID.

A ideia do SOLID é tirar ainda mais proveito da orientação a objetos a fim de resolver problemas comuns relacionados a código em projetos de software. Na Zup Edu gostamos de pensar que **SOLID discute, extrai e aponta o melhor do Polimorfismo na OO, o que nos permite entender o real poder desse pilar de forma isolada e em termos de arquitetura de código**. Por esse motivo, se você aprendeu bem sobre OO com conteúdo que curamos até aqui então com toda certeza você se sentirá bastante confortável nos estudos de SOLID.

Por fim, vale a pena refletirmos sobre SOLID de uma maneira mais crítica, afinal tudo em engenharia de software possui prós e contras. Ou seja, será que SOLID é tão "solid" assim? 🤔

### 3.1. Conteúdo teórico

1. [Clean Code e SOLID com Alberto Souza](https://www.youtube.com/watch?v=XV9B4LX_re8&ab_channel=Alura) (16min)
2. [Zupcast #55: Desbravando SOLID com Alexandre Aquiles](https://www.zup.com.br/zupcast/55-desbravando-solid) (37min)
3. [SOLID Principles: melhorando o design do seu código](https://www.zup.com.br/blog/design-principle-solid) (10min)
4. [SOLID para devs de alta performance](https://www.zup.com.br/blog/solid-devs-de-alta-performance) (15min)
5. [SOLID: Programação Orientada a Objetos](https://www.zup.com.br/webinars/webinar-solid-programacao-orientacao-a-objetos) (1h)
6. [Why SOLID principles are still the foundation for modern software architecture](https://stackoverflow.blog/2021/11/01/why-solid-principles-are-still-the-foundation-for-modern-software-architecture/) (12min)
7. [The Principles of OOD](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod) (20min)
8. [Solid Relevance](https://blog.cleancoder.com/uncle-bob/2020/10/18/Solid-Relevance.html) (15min)
9. [Livro Desbravando SOLID - Alexandre Aquiles](https://www.casadocodigo.com.br/products/livro-desbravando-solid) (4-6h)
10. [Livro Orientação a Objetos e SOLID para Ninjas - Mauricio Aniche](https://www.casadocodigo.com.br/products/livro-oo-solid) (4-6h)
11. [Que tal contrapontos? 😈 Livro SOLID is not SOLID - David Bryant Copeland](https://solid-is-not-solid.com/) (3-6h)

### 3.2. Como posso me avaliar?

Mais uma rodada para validarmos nosso conhecimento e fortalecer as conexões do que estudamos.

#### **❓Atividade 1**:

Aqui temos 2 possibilidades de tarefas, **escolha a que achar mais interessante para exercitar seu aprendizado** (mas se quiser você pode fazer as duas 😎):

- a) Se possível, encontre um trecho de código no seu atual projeto e refatore-o aplicando algum dos principios SOLID. Em seguida, crie um [Gist](https://gist.github.com/) com a versão de antes e depois da refatoração, e compartilhe-o no [nosso fórum do Github](https://github.com/rafaelpontezup/grupo-plano-de-estudos-qualidade-de-codigo/discussions);
- b) Escolha um dos principios SOLID e escreva um artigo sobre ele de tal forma que um desenvolvedor(a) junior possa utiliza-lo como fonte de aprendizado. Aqui é importante ser didático e apresentar bons exemplos de código;

>⚠️ **Lembre-se de compartilhar seu artigo**<br/>
> Você pode escrever o artigo onde você achar melhor (como Gist, Google Docs, blog pessoal etc), o importante é que você consiga compartilhá-lo com nossa turma e monitor através de um link público no [nosso forum do Github](https://github.com/rafaelpontezup/grupo-plano-de-estudos-qualidade-de-codigo/discussions) 😊

#### **❓Atividade 2**:

Por fim, se você ainda não fez nossa avaliação [**Knowledge about SOLID Design Principles**](https://hr.gs/badge-knowledge-about-solid-design-principles) ou se não obteve êxito nela, essa é uma excelente oportunidade para (re)fazê-la.

[Acesse o link da avaliação](https://hr.gs/badge-knowledge-about-solid-design-principles) e valide seus conhecimentos sobre os principios de design SOLID! 🎯

## 4. Design e arquitetura de código

Ao começar um novo projeto de software você precisará definir qual arquitetura de código você adotará no seu projeto. Ter uma arquitetura bem definida guiará o time na hora de desenvolver novas funcionalidades, na hora de navegar e encontrar artefatos na base de código existente mais rapidamente e, principalmente, a mantê-la por médio-longo prazo de forma sustentável.

Existe diversos estilos arquiteturais, mas sem dúvida, hoje em dia os estilos arquiteturais mais populares e utilizadas no mundo Java são Clean Architecture e Hexagonal Archicteture. Mas será que eles são ideais para todo tipo de projeto, incluindo microsserviços? Quais os pontos fortes e fracos delas? Onde elas ajudam e, principalmente, onde elas podem atrapalhar? 🤔

Será que depois de todo conhecimento e aprendizado sobre OO, design patterns e principios de design SOLID o estilo arquitetural importa tanto assim? Será que estou olhando pro lugar certo? 🤔

### 4.1. Conteúdo teórico

1. Hexagonal Architecture
    - 1.1. [Hexagonal architecture - Alistair Cockburn](https://alistair.cockburn.us/hexagonal-architecture/) (15min)
    - 1.2. [Treinamento na Handora: Introdução a arquitetura Hexagonal](https://handora.zup.com.br/treino-completo/11) (4-6h)
2. Clean Architecture
    - 2.1. [Clean Architecture: descubra o que é e onde aplicar Arquitetura Limpa](https://www.zup.com.br/blog/clean-architecture-arquitetura-limpa) (15min)
    - 2.2. [What are the main differences between Clean Architecture and Hexagonal Architecture](https://www.gregorypacheco.com.br/posts/differences-between-clean-architecture-and-hexagonal-architecture-cshrp-dot-net.html) (15min)
3. Nem Hexagonal nem Clean Architecture
    - 3.1. [PresentationDomainDataLayering - Martin Fowler](https://martinfowler.com/bliki/PresentationDomainDataLayering.html) (10min)
    - 3.1. [Layered architecture pattern in software engineering](https://thecodereaper.com/2020/08/22/layered-architecture-pattern-in-software-engineering/) (15min)
    - 3.1. [Package by Feature 🤯](https://phauer.com/2020/package-by-feature/) (15min)
    - 3.2. [Package by feature, not layer](http://www.javapractices.com/topic/TopicAction.do?Id=205) (10min)
    - 3.3. [Package by Layer vs Package by Feature](https://medium.com/sahibinden-technology/package-by-layer-vs-package-by-feature-7e89cde2ae3a) (15min)
    - 3.4. [Discussão entre especialistas no Spaces do Twitter sobre “Clean Arch morreu?” 🤯😈](https://twitter.com/alex_aquiles/status/1557105442723172354) (1h32min)
    - 3.5. [Overengineering in Clean/Onion/Hexagonal Architectures 🤯](https://victorrentea.ro/blog/overengineering-in-onion-hexagonal-architectures/) (15min)

### 4.2. Como posso me avaliar?

Essa atividade vai exigir um pouco mais de você, mas com certeza vai te ajudar a solidificar o que estudamos sobre estilos arquiteturais e vai te dar "pano pra manga" para discutir com sua turma, monitor e, quem sabe, até com seu time 😈

#### **❓Atividade 1**:

Crie um novo projeto de microsserviço onde você consiga aplicar o estilo arquitetural Package by Feature. A ideia é você escrever esse serviço aplicando este estilo arquitetural e poder enxergar os prós e contras com outros estilos arquiteturais mais rebuscados. 

Para melhor proveito dessa atividade, é obrigatório que seu serviço possua no minimo 2 features. Melhor ainda se ele contiver 3 ou 4 features, assim você pode praticar mais e reforçar o aprendizado 💪🏻

Lembre-se de compartilhar o projeto no [nosso fórum do Github](https://github.com/rafaelpontezup/grupo-plano-de-estudos-qualidade-de-codigo/discussions) para feedback e possíveis discussões!

#### **❓Atividade 2**:

Se você ainda não fez nossa avaliação [**Knowledge about Hexagonal Architecture**](https://hr.gs/badge-knowledge-about-hexagonal-architecture) ou se não obteve êxito nela, essa é uma excelente oportunidade para (re)fazê-la.

[Acesse o link da avaliação](https://hr.gs/badge-knowledge-about-hexagonal-architecture) e valide seus conhecimentos sobre Arquitetura Hexagonal! 🎯

#### **❓Atividade 3**:

Por fim, se você ainda não fez nossa avaliação [**Knowledge about Clean Architecture**](https://hr.gs/badge-knowledge-about-clean-architecture) ou se não obteve êxito nela, essa é uma excelente oportunidade para (re)fazê-la.

[Acesse o link da avaliação](https://hr.gs/badge-knowledge-about-clean-architecture) e valide seus conhecimentos sobre Arquitetura Limpa! 🎯

