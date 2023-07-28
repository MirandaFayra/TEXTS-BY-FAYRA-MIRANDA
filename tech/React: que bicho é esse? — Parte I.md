
## _React: que bicho é esse? — Parte I?_

Conceitos iniciais sobre uma das tecnologia base do desenvolvimento front-end ~ Por [Fayra Miranda]
 
Texto escrito em Nov 19, 2021 para o Medium da Dupla Tech ~ Acesse o [link][dupla-transicao]
 
 ------
Como vimos anteriormente, a linguagem JavaScript é uma das mais utilizadas no mercado de tecnologia devido às suas diversas vantagens.

Diariamente, uma nova ferramenta baseada nessa linguagem é lançada tendo como intuito facilitar o processo de desenvolvimento das aplicações e também otimizar o tempo.

Nesse artigo, vamos aprofundar um pouco mais em uma das tecnologias citadas no último texto: a biblioteca React para desenvolvimento front-end.

## Diferença entre biblioteca e framework
Ao longo deste texto, mencionaremos dois conceitos fundamentais: o de Biblioteca e o de Framework. Para muitas pessoas a diferença entre eles é um pouco confusa. De modo geral, podemos definir cada um deles como:

**Framework →** Conjunto de soluções (classes abstratas, objetos e padrões), tendo como principais objetivos sanar problemas habituais e permitir a reusabilidade, em uma arquitetura extensível e flexível.

**Biblioteca →** Coleção de recursos (dados de configuração, documentação, procedimentos, templates, etc…) cujo o intuito é trabalhar de forma independente de onde será implementado. Ou seja, é possível atualizar uma biblioteca sem alterar o programa principal.

## A origem do React
A história do React está relacionada com o desenvolvimento do Facebook.

Em 2011, as pessoas desenvolvedoras responsáveis pelo Facebook passaram a ter dificuldades com a manutenção dos códigos. Conforme os recursos do Facebook Ads se tornavam mais complexos, era necessário um número maior de pessoas para realizar a manutenção do código.

O aplicativo havia se tornado difícil de manusear devido às diversas atualizações em cascatas realizadas e estava extremamente complicado acompanhar o desenvolvimento do código. Portanto, era necessário tomar uma providência urgente para tornar o código da aplicação mais eficiente. Além disso, haviam alguns problemas em relação à experiência do usuário com o aplicativo.

Pensando nesses diversos problemas, o engenheiro Jordan Walke do Facebook cria FaxJS um protótipo que tornou os processos mais eficientes.

_E assim nasce o React_

Em maio de 2013, no evento JS ConfUS, React é rebatizado e torna-se open source, possibilitando amplo acesso para a comunidade desenvolvedora.

## Como funciona o React

React é definido como:

> (…) uma biblioteca JavaScript declarativa, eficiente e flexível para criar interfaces com o usuário. Ele permite compor UIs complexas a partir de pequenos e isolados códigos chamados “componentes”.

_Em outras palavras, essa ferramenta é uma biblioteca front-end em JavaScript focada em criar de forma mais fácil interfaces para os usuários. Com pequenos e isolados trechos de código, pode-se criar interfaces completas._

O React se baseia no conceito de componentização, ou seja dividir suas aplicações em partes independentes, isoladas e reutilizáveis. Para isso, toda a lógica é escrita em JavaScript. Essas características permitem a construção de aplicações de grande porte, de forma rápida e escalável.

## Conceitos básicos do React
No React, há alguns conceitos básicos que são essenciais para a sua aprendizagem e para você dar os primeiros passos.

## JSX
JSX foi criado pelo mesmo time desenvolvedor do React. A sigla é um acrônimo para JavaScript XML, ou seja, uma extensão de sintaxe para JavaScript. Seu principal objetivo é facilitar a criação de componentes dentro do React.

Sua sintaxe permite que o HTML co-exista no mesmo arquivo com o JavaScript. Com isso, é possível escrever de forma simples os componentes.

O JSX precisa de um transpilador para transformar em JavaScript e ser interpretado pelo navegador. Uma das ferramentas mais utilizadas para transpilar o código é o babel.

Portanto, o JSX possibilita maior facilidade para escrever, ler e interpretar os códigos.

Agora que já falamos da parte teórica, vamos mostrar em código como seria isso.

Abaixo, temos um exemplo de como seria o código sem o JSX:

![Imag1 React](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/00b5fc45-e906-48d0-a439-b6fc8ed5154a)

_Imagem 1 -Fonte : Elaborado pela Autora_

Utilizando o JSX o código fica dessa forma:

![Imagem2](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/cdf63ad4-2281-413e-b4ec-e971a2db168a)


_Imagem 2 -Fonte : Elaborado pela Autora_

Portanto, dá para perceber a facilidade que o JSX nos traz, além de permitir a utilização de expressões no meio de texto de forma prática.

## Componentes
Para explicar componentes, vamos fazer aqui uma alusão às aulas de biologia. Quando falamos da organização do corpo humano, podemos dividi-lo em pequenas partes. Mas Fay, como assim biologia e programação? Eu que não gosto de biologia, o que eu faço? Calma, vou explicar nas próximas linhas e te ajudar a abstrair e entender os conceitos. 😉

A primeira parte que nos forma como seres humanos são as células, como por exemplo a célula muscular. A junção das células forma os tecidos, ou seja, várias células musculares associadas podem formar o músculo estriado cardíaco. Os tecidos, ao se agruparem formam o órgão (no caso do músculo estriado cardíaco, juntamente com outros tecidos formará o coração). A união dos órgãos, formam sistemas (no nosso exemplo anterior, teremos o sistema cardiovascular). Os diversos sistemas do nosso corpo (circulatório, esquelético, nervoso, muscular etc…) juntos, formam o organismo (ou seja, você que está lendo esse texto).

Resumidamente, algo macro é formado por pequenas partes menores. Essa definição pode ser aplicada para o conceito de Componentes no React.

![Imagem3](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/8d63101f-4e7c-4aae-b7c1-18e9ebe325b3)



_Imagem 3 -Fonte : Elaborado pela Autora_

Falando de forma mais técnica, um componente em React pode ser definido como:

> “ (…) componentes são como funções JavaScript. Eles aceitam entradas arbitrárias (chamadas “props”) e retornam elementos React que descrevem o que deve aparecer na tela.”

A lógica de construção dos Componentes em React é criar pequenas partes independentes e reutilizáveis, facilitando a construção, organização e manutenção do código. Para isso, o componente precisa seguir duas principais características : aceitar um parâmetro de propriedade (props) e retornar um React Element.

Imaginemos que desejamos fazer um botão para nossa página:

![Imagem4](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/9d0b8712-0696-40d5-9c7e-67aec01c0e18)


_Imagem 4 -Fonte : Elaborado pela Autora_

Há dois modos de elaborar componentes em React, são eles: componente funcional e componente de classe.

Os componentes funcionais levam esse nome pois são declarados em formato de funções Javascript. Os de classe, por outro lado, são criados baseados no conceito de classe do Javascript. Mas como ficaria essa diferença em código?

##### Componente Funcional

![Imagem5](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/86fc2b37-be90-4d89-a2f0-dd854392213a)


_Imagem 5 -Fonte : Elaborado pela Autora_

Algumas características dos componentes funcionais:

- Não têm o estado e nem ciclo de vida direto (utiliza-se os Hooks)
- Não possuem o método render ( )
- Não utilizam os construtores.

#####  Componente de Classe

![Imagem6](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/74c6d53a-08e6-479a-bd30-970388cc994f)

_Imagem 6 -Fonte : Elaborado pela Autora_

Algumas características dos componentes classe:

- Possuem o método render ( )
- Têm estado e ciclo de vida
- Usam o construtor.

Como podemos ver, os componentes de classe são bem mais verbosos que os funcionais. Atualmente, o mais utilizado é o componente funcional. Caso queira saber mais sobre os dois componentes, recomendo muito ler esses [dois] textos [aqui].

## Props
Esse próximo conceito geralmente tende a gerar muita confusão em quem está começando a desenvolver no React. Props são propriedades (informações) as quais desejamos passar de um local (componente) para o outro. Essas informações podem possuir diversos formatos (strings, números, funções, etc…).

Uma das principais utilidades desse recurso é auxiliar na exibição de dados ou proporcionar a interação entre os componentes para dinamizá-los.

#### Props em Componentes Funcionais

![Imagem7](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/a0cbbcba-9da6-4cc5-824a-709da0ada48b)

_Imagem 7 -Fonte : Elaborado pela Autora_

#### Props em Componentes de Classe
![Imagem8](https://github.com/MirandaFayra/TEXTS-BY-FAYRA-MIRANDA/assets/52434685/ee6b49b1-fe32-435a-98f7-5d91650139b1)


_Imagem 8 -Fonte : Elaborado pela Autora_

Caso você deseje se aprofundar mais e entender o passo a passo de como passar props, recomendo a leitura [desse artigo].

Até aqui, vimos diversos conceitos importantes e essenciais do React. Vamos dar uma “pausinha” para você, minha querida pessoa leitora, conseguir assimilar e pesquisar mais sobre os conteúdos .

No nosso próximo texto, vamos não somente continuar explicando um pouco mais do React e seus conceitos fundamentais, como também dicas para estudar essa tecnologia. Até lá! 😉



_Referências:_

- BÓSON TREINAMENTOS. O que é uma Biblioteca em Programação (25/02/2021). Disponível em: https://www.youtube.com/watch?v=x5Ug7SVcnGU. Acesso em: 6 nov. 2021.

- CÓDIGO FONTE TV. JSX // Dicionário do Programador (24/05/2021). Disponível em: https://www.youtube.com/watch?v=lP8ac9fw72c . Acesso em: 6 nov. 2021.

- CÓDIGO FONTE TV. React.JS // Dicionário do Programador (21/09/2020). Disponível em: https://www.youtube.com/watch?v=Ri76yOpLrNg . Acesso em: 6 nov. 2021.

- FELIPE GALVAO. Aprenda React — Componentes, State e Props. Disponível em: https://felipegalvao.com.br/pt/blog/learn-react-components-state-and-props/. Acesso em: 12 nov. 2021.

- KENZIE. React: o que é, como funciona e porque usar e como aprender. Disponível em: https://kenzie.com.br/blog/react/. Acesso em: 6 nov. 2021.

- REACT ENLIGHTENMENT. What Is JSX?. Disponível em: https://www.reactenlightenment.com/react-jsx/5.1.html. Acesso em: 12 nov. 2021.

- REACT. Componentes e Props. Disponível em: https://pt-br.reactjs.org/docs/components-and props.html. Acesso em: 6 nov. 2021.

- REACT. Introdução. Disponível em: https://pt-br.reactjs.org/docs/getting-started.html. Acesso em: 6 nov. 2021.

- RISINGSTACK. The History of React.js on a Timeline. Disponível em: https://blog.risingstack.com/the-history-of-react-js-on-a-timeline/. Acesso em: 13 nov. 2021.

- STACKOVERFLOW.2020 Developer Survey. Disponível em: https://insights.stackoverflow.com/survey/2020#developer-profile.Acesso em: 6 nov. 2021.

- TABLELESS.O Guia Completo do React e o seu Ecossistema.Disponível em: https://tableless.com.br/guia-completo-react-ecossistema/. Acesso em: 6 nov. 2021.


….

Gostou do que leu? Então não se esqueça de dar mais de 50 claps e curtir nossas redes. É um pequeno gesto mas que auxilia este conteúdo impactar a vida de mais mulheres ❤


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

 
   [Fayra Miranda]: <https://www.linkedin.com/in/fayramiranda/>
   [dupla-transicao]: <https://medium.com/@Dupla/6%C2%BA-texto-react-que-bicho-%C3%A9-esse-parte-i-8891f81e9981>
   [texto]: <https://medium.com/@Dupla/javascript-o-que-%C3%A9-onde-est%C3%A1-b45aa6fb10ff>
   [dois]: <https://blog.geekhunter.com.br/criando-componentes-react-componentes-de-classe-e-funcional-sem-estado/>
   [aqui]: <https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components-in-react/>
   [desse artigo]: <https://www.digitalocean.com/community/tutorials/how-to-customize-react-components-with-props-pt>
   
