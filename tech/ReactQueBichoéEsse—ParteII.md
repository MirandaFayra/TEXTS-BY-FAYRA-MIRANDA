
## _React: que bicho é esse? — Parte II_

Conceitos iniciais sobre uma das tecnologia base do desenvolvimento front-end ~ Por [Fayra Miranda]
 
Texto escrito em Dez 2, 2021 para o Medium da Dupla Tech ~ Acesse o [link][dupla-transicao]
 
 ------

 No nosso último [texto], falamos sobre uma das bibliotecas mais famosas em Javascript para front-end da atualidade, o React.

Nesse texto, vamos continuar abordando alguns conceitos essenciais para a compreensão dessa biblioteca, além de auxiliar na construção de uma base sólida em React.

Alguns tópicos que já sabemos, baseado na nossa leitura anterior: A diferença entre biblioteca e framework; a origem do React; como o React funciona; o que é JSX; o que são Componentes e o que são Props.

Caso não tenha lido o último texto, recomendo fortemente lê-lo para conseguir entender os conteúdos que abordaremos nas próximas linhas.

## Estado
Para explicar estado, vamos usar a analogia de conta bancária (com valores aleatórios, só para facilitar a compreensão).

Imagina que recebemos o nosso primeiro salário como pessoa desenvolvedora Jr. Após um mês de trabalho, acabamos de ganhar R$4.000,00. Tiramos R$1.000,00 e investimos esse valor. Do valor restante (R$3.000,00), pagamos R$2.500,00 de contas, e usamos R$500,00 para comprar um curso novo e nos mantermos atualizadas em relação a tecnologias. Ou seja, nossa conta é um local onde além de guardarmos as informações, fazemos alterações.

Em poucas palavras, como já bem definido nesse texto o estado (state) de um componente React é:

> “ (…) O estado (state) de um componente React tem uma função muito simples e específica. Ele é uma propriedade do componente onde colocamos dados que, quando mudados, devem causar uma nova renderização (...)"

Como no exemplo da nossa conta, o estado no React guarda as informações e alterações.

Agora que já sabemos o conceito de estado, podemos explicar a divisão dos componentes em React. Os mesmos podem ser divididos em duas categorias: os Sem Estado (Stateless) e os Com Estado (Stateful).

Para os componentes sem estado, é importante apenas a apresentação dos dados. Logo, a utilização do estado se faz irrelevante. Por outro lado, os componentes do tipo Stateful (com estado), além da apresentação dos dados ser extremamente importante, os estados estão responsáveis por alguma lógica ou transformação dos dados.

Uhmmmm, na teoria fez sentido! Como isso funciona na prática?

Para exemplificar tudo isso, vamos criar um estado cujo intuito seja guardar o nome de uma das candidatas inscritas em nossa página. Podemos criar um estado chamado nomePessoaInscrita, que guardará o nome Nathalia.

Em código ficaria assim:

#### Criando o estado.

_Imagem 1 -Fonte : Elaborado pela Autora_

Agora, como vemos abaixo, podemos acessar o valor e mostrar na tela a informação do nome.

#### Acessando a informação

_Imagem 2 -Fonte : Elaborado pela Autora_

É importante destacar que esse modo de declaração é utilizado nos componente de classe. Caso desejemos usar estado em um componente funcional, optamos pelo hook useState (quem sabe no futuro, escrevamos um artigo sobre Hooks).

## Ciclo de Vida
Um conceito bem interessante do React é o de Ciclo de Vida. Para explicar e entender a importância do Ciclo de Vida nos componentes React, podemos associar com o próprio ciclo de vida de um ser humano.

Nascemos, crescemos, nos reproduzimos (ou não) e quando acaba nossa trajetória aqui, morremos. Assim como nós, as aplicações também possuem um ciclo de vida. Ela é construída (nasce), atualizada (crescimento) e morre.

Os métodos de Ciclo de Vida no React, possibilitam a criação e alterações nas diversas etapas do componente (montagem, atualização e desmontagem).

**O ciclo de um componente React passa por quatro fases. A primeira, é a inicialização do componente, onde configuramos os estados iniciais e as props (caso sejam existentes)**. Após essa etapa onde preparamos a base, podemos montar o componente. Na **segunda etapa (Montagem)** , podemos chamar métodos que serão invocados pré e pós montagem do componente.

#### Pré-montagem do Componente

Como podemos ver nesse artigo, caso desejemos **fazer alguma alteração antes do componente ser montado, devemos colocá-las no método componentWillMount**.

> “(…) Todas as coisas que você desejar fazer antes do componente ser montado, devem ser definidas aqui. Este método é executado uma vez em um ciclo de vida de um componente e antes da primeira renderização. (..)”

Outro método usado nessa etapa, é o **render**. Ele é utilizado para montar o componente no navegador.

## Pós-montagem do Componente

Após a montagem e sua primeira renderização, é executado o método **componentDidMount**. Geralmente, no front-end consumimos alguns serviços de APIs (como por exemplo, um mapa do Google Maps que vemos em aplicativos de mobilidade). Em aplicações React, caso desejemos consumir alguma API, é feito no **componentDidMount**.

Para entendermos um pouco mais sobre o componentDidMount, vamos utilizar a explicação desse artigo.

> “ (…) Este método é executado uma vez em um ciclo de vida de um componente e será após a primeira renderização. Com esse método podemos acessar o DOM, devemos inicializar bibliotecas JS como D3 ou Jquery, que precisa acessá-lo (…)”

Como mencionamos anteriormente, após a montagem do componente temos sua atualização. No React, podemos atualizar de duas formas distintas o componente tanto no estado, como por props. Alguns **métodos disponíveis na etapa de atualização do componente**:

- **ComponenteWillUpdate ⇒** Prepara para a próxima renderização. Geralmente, é usado para quando é necessário alguma preparação antes da renderização de algum item.

- **ComponenteDidUpdate ⇒** esse método é executado quando um novo componente foi atualizado.

Há diversos outros métodos na etapa de atualização. Caso você queira se aprofundar mais, recomendo fortemente a leitura deste [artigo].

A fase final de um componente é a desmontagem, ela ocorre quando o componente não é mais necessário. Nesse momento, usamos o método **componentWillUnmount**.

Talvez, tudo isso possa ter parecido muito abstrato quando explicado em texto. Pensando nisso, trouxe aqui um diagrama para facilitar o entendimento dos métodos de ciclo de vida mais utilizados 🤗 Caso queira consultar de forma mais interativa, é só acessar [esse link].

_Imagem 3 -Fonte : https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/_

**Resumindo**: Há três momentos importantes ao longo da “vida” de um componente. São eles: montagem (renderiza o componente pela primeira vez), atualização (alterações de informação via props ou estado) e desmontagem (antes de finalizar a renderização do componente na tela). Em cada uma dessas etapas, usamos métodos para realizar ações.

## Virtual Dom
No desenvolvimento front-end moderno, uma das práticas mais comuns é a manipulação do DOM. Mas o que é DOM? E o que isso tem a ver com o React?

Primeiramente, precisamos definir aqui esse conceito super importante . Segundo o Mozila, DOM pode ser definido como:

> “ O Modelo de Objeto de Documento (DOM) é uma interface de programação para documentos HTML, XML e SVG. Ele fornece uma representação estruturada do documento como uma árvore. O DOM define métodos que permitem acesso à árvore, para que eles possam alterar a estrutura, estilo e conteúdo do documento (…)”

**Resumidamente, o DOM permite que os navegadores e scripts manipulem o conteúdo de uma página Web.**

Porém, há alguns problemas na manipulação do DOM. A principal de todas é relacionado a performance, pois cada acesso ao DOM leva um certo tempo além de obrigar o navegador a renderizar novamente o local onde foram feitas as alterações. Com isso, a manipulação direta do DOM tende a ser mais lenta que a maioria das operações realizadas pelo JavaScript.

Pensando nesse problema e em outros, o time do Facebook criou o Virtual DOM para a nossa querida biblioteca React.

Segundo esse artigo, Virtual DOM pode ser definido como:

> “ (…) é uma representação do DOM mantida em memória. Assim, quando precisamos fazer alguma alteração, ela é feita no Virtual DOM, que é bem mais rápido que o DOM. Com isso ele analisa todos os lugares que serão afetados e sincroniza com o DOM em um processo chamado Reconciliação. (…)”

Portanto, é criado no React uma cópia dos nós (nodes) do DOM em JavaScript. **Após esse processo, as manipulações são realizadas no virtual DOM tornando o processo mais rápido**. Ou seja, apenas é alterado diretamente o DOM caso haja necessidade.

Como os dois conceitos mencionados se conectam no React? Simples, as alterações feitas via Métodos de Ciclo de Vida são realizadas no Virtual Dom.

O intuito dos nossos dois últimos artigos foi fundamentar a base teórica do React para te auxiliar a ganhar independência nos futuros estudos e pesquisas.

Como esse texto já está muito extenso (além de conter diversas definições complexas), vamos terminá-lo por aqui para você poder digerir todas as informações. No nosso próximo texto, vamos dar dicas de estudos sobre essa tecnologia. Até lá! 😉


_Referências:_

- COD3R. Termos Básicos — React . Disponível em : https://blog.cod3r.com.br/termos-basicos-react/ . Acesso em: 20 nov. 2021.

- DIMAS CYRIACO. Entendendo o estado no React. Disponível em : https://medium.com/@dimascyriaco_29717/entendendo-o-estado-no-react-ac1e5c32b0c0 . Acesso em: 21 nov. 2021.

- EDMO LIMA.Métodos do ciclo de vida de componentes ReactJS — Um mergulho profundo!Disponível em :https://medium.com/creditas-tech/métodos-do-ciclo-de-vida-de-componentes-reactjs-um-mergulho-profundo-332ed7b3b782 Acesso em: 21 nov. 2021. 

- MDN WEB DOCS. Modelo de Objeto de Documento (DOM). Disponível em : https://developer.mozilla.org/pt-BR/docs/Web/API/Document_Object_Model .Acesso em: 21 nov. 2021.

- TABLELESS . O Guia Completo do React e o seu Ecossistema — Você ouve falar frequentemente sobre o React mas sabe pouco sobre ele? . Disponível em : https://tableless.com.br/guia-completo-react-ecossistema/ .Acesso em: 21 nov. 2021. 

- TREINAWEB . O que é DOM, Virtual DOM e Shadow DOM? — Entenda o que realmente é o DOM e sua diferença em relação ao Virtual DOM e Shadow DOM. Disponível em : https://www.treinaweb.com.br/blog/o-que-e-dom-virtual-dom-e-shadow-dom .Acesso em: 21 nov. 2021. 


….

Gostou do que leu? Então não se esqueça de dar mais de 50 claps e curtir nossas redes. É um pequeno gesto mas que auxilia este conteúdo impactar a vida de mais mulheres ❤


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

 
   [Fayra Miranda]: <https://www.linkedin.com/in/fayramiranda/>
   [dupla-transicao]: <https://medium.com/@Dupla/react-que-bicho-%C3%A9-esse-parte-ii-bb309eef614f>
   [texto]: <https://medium.com/@Dupla/react-que-bicho-%C3%A9-esse-parte-ii-bb309eef614f>
   [dois]: <https://blog.geekhunter.com.br/criando-componentes-react-componentes-de-classe-e-funcional-sem-estado/>
   [aqui]: <https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components-in-react/>
   [desse artigo]: <https://www.digitalocean.com/community/tutorials/how-to-customize-react-components-with-props-pt>
   [artigo]: <https://medium.com/creditas-tech/m%C3%A9todos-do-ciclo-de-vida-de-componentes-reactjs-um-mergulho-profundo-332ed7b3b782>
   [esse link]: <https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/>
   
