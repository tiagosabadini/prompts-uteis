## Testando o modelo com e sem contexto
O objetivo é entender o comportamento do LLaVA:7b rodando localmente. Os prompts foram usados com técnicas de Zero, One e Few Shot. 

```bash
Pergunta: O que é uma maça?
Resposta: Una maça, também chamada de martelo, é uma ferramenta utilizada para golpir ou abrir materiais como metais, pedra ou madeira.
Ela pode ser manual ou mecânica e pode ter vários tipos, como maça de bola, de cabo e de vibro.
A forma e tamanho da cabeça da maça podem variar, dependendo do material que a ferramenta irá abrir.
```

```bash
Pergunta: O que é uma maçã?
Resposta: A palavra "maçã" não existe na língua portuguesa.
No entanto, poderia ser confundida com a palavra "maca", que significa "massa" ou "bola de massa".
Por exemplo, em Portugal, as pessoas podem dizer "uma maca" para se referir a uma esfera, um globo ou um corpo redondo.
```
### Aqui ainda usando a palavra maça sem acento, porém com contexto
A resposta contém muitos erros e imprecisões, mas ele entendeu que estava falando de uma maçã, fruta.
```bash
Pergunta: Você é um nutricionista especializado em dieta de frutas. Me explique em tópicos quais as características de uma maça e quais os benefícios dessa fruta para o corpo humano.
Resposta: A maça é uma das frutas mais conhecidas e comuns na dieta. É um tipo de fruta que tem origem no sudoeste do Brasil, mas foi introduzida em outras partes do mundo como resultado de sua cultura e reprodução a partir de germen.

As características principais da maça são:

Cor: a maça é geralmente vermelha ou rosa quando madura e branca ou amarela quando imatura. O seu cor varia dependendo do tipo de maça.
Forma: possui forma oval, com um comprimento pequeno e largura maior, e uma pele fina e rústica.
Sabor: tem sabor doce e um leve cheiro de amêndra quando está madura.
Textura: a maça tem uma pele suave e uma textura firme e granulosa no interior.
Continentes: é nativa na América do Sul, mais especificamente na região que hoje corresponde ao Brasil, Argentina, Uruguai e Paraguai.
Os benefícios da maça para o corpo humano são muitos, incluindo:

Riqueza em vitaminas: a maça é uma fruta rica em vitaminas, como vitamina C, que tem papel importante na saúde. A vitamina C é um antioxidante natural, ajudando o organismo a combater as reações oxidativas e proteger o corpo contra doenças inflamatórias.
Nutriente rico: a maça é uma fruta rica em nutrientes como fósforo, potássio, magnesio e manganês. Esses nutrientes são importantes para a saúde geral, pois podem contribuir para a resistência contra doenças infectocontagiosas e a funcionalidade das células do corpo.
Ajudando na prevenção de doenças: o ácido malônico, presente em maças vermelhas, pode ajudar no controle da glutenose no sangramento, possivelmente reduzindo o risco de doenças relacionadas ao azúcar, como diabetes.
Antiinflamatórios: as maças são conhecidas por conter ácido benolico, um composto com propriedades antiinflamatórias e que pode ajudar na prevenção de doenças inflamatórias.
Em resumo, a maça é uma fruta saudável e nutricionalmente valiosa para a alimentação humana, oferecendo muitos benefícios para a saúde geral da população.
```
