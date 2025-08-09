# livro-gps-tracking
# Livro: "Principles-of-GNSS-inertial-and-multi-sensor-integrated-navigation-systems"

## Capítulo 1- Introduction

*  Global navigation satellite systems (GNSS)
*  Global Positioning System (GPS


### 1.1 What is Navigation ?

Uma técnica de navegação é um método para determinar posição e velocidade, manual ou automaticamente. Um sistema de navegação, às vezes conhecido como auxílio à navegação, é um dispositivo que determina posição e velocidade automaticamente. A saída de um sistema ou técnica de navegação é conhecida como solução de navegação.

Um sensor de navegação é um dispositivo usado para medir uma propriedade a partir da qual o sistema de navegação calcula
sua solução de navegação; exemplos incluem acelerômetros, giroscópios e receptores de radionavegação.

A solução de navegação representa o sistema de coordenadas do corpo de navegação (por exemplo, uma aeronave, navio, carro ou pessoa) em relação a um sistema de coordenadas de referência. Uma referência comum é a Terra. Os componentes dos vetores que compõem a solução de navegação podem ser resolvidos em torno dos eixos de um terceiro sistema de coordenadas
(por exemplo, norte, leste e para baixo). Os sistemas de navegação frequentemente utilizam um referencial rotativo para corresponder à rotação da Terra.

Posicionamento é a determinação da posição de um corpo, mas não de sua velocidade ou atitude. Muitas tecnologias de navegação, embora sejam estritamente sistemas de posicionamento,
operam a uma taxa alta o suficiente para que a velocidade seja derivada da taxa de variação
da posição.

O rastreamento ou vigilância difere da navegação, pois as informações de posição e velocidade são obtidas por terceiros, sem necessariamente utilizar equipamentos a bordo do objeto rastreado. No entanto, um sistema de rastreamento pode ser usado para navegação simplesmente transmitindo as medições de posição e velocidade para o objeto que está sendo rastreado. Da mesma forma, um sistema de navegação pode ser usado para rastreamento, transmitindo a solução de navegação para uma estação de rastreamento.

### 1.1.1 Position Fixing

A correspondência de recursos compara recursos no local atual, como pontos de referência ou altura do terreno, com um mapa para determinar a posição atual. Position Fixing também podem ser obtidas medindo-se os alcances e/ou a direção de objetos conhecidos. Isso é ilustrado, para o caso bidimensional, pela Figura 1.1, em que X marca a posição desconhecida do usuário e A e B, as posições conhecidas de dois objetos de referência.

Um componente de um sistema de fixação de posição externo ao equipamento do usuário é conhecido como auxílio à navegação (AtoN- aid to navigation). AtoNs incluem pontos de referência, como luzes, e sinais de radionavegação.

### 1.1.2 Dead Reckoning
Mede a mudança de posição ou mede a velocidade e a integra. Isso é adicionado à posição anterior para obter a posição atual.

A velocidade ou distância percorrida é medida no sistema de coordenadas do corpo, portanto, uma medição de atitude separada é necessária para obter a direção de deslocamento no sistema de referência. Para navegação bidimensional, uma medição de rumo é suficiente, enquanto para navegação tridimensional, uma medição completa de atitude em três componentes é necessária.

Quando a atitude muda, quanto menor o passo no cálculo da posição, mais precisa será a solução de navegação. Os cálculos eram originalmente realizados manualmente, limitando severamente a taxa de dados, mas agora são feitos por computador.

Hoje, a contagem de passos pode ser automatizada usando um pedômetro, enquanto técnicas mais sofisticadas de estimativa de pedestres (PDR) usando acelerômetros também determinam o comprimento do passo. Um odômetro mede a distância contando as rotações de uma roda.

Os métodos contemporâneos de medição de velocidade incluem o radar Doppler [3] e a integração de medições de acelerômetro em um sistema de navegação inercial. A altura pode ser calculada a partir de medições de pressão usando um altímetro barométrico (baro). Um altímetro de radar (radalt) mede a altura acima do terreno, podendo ser usado para determinar a altura de uma aeronave onde a altura do terreno é conhecida.

Como o INS obtém atitude integrando medições de taxa angular feitas por giroscópios.

A estimativa requer uma posição inicial conhecida, mas depois disso fornecerá uma solução de navegação ininterrupta, exceto em caso de falha do equipamento.

### 1.2 Inertial Navigation

Um inertial navigation system (INS), as vezes conhecido como inertial navigation unit (INU). É um sistema completo de navegação por estimativa tridimensional.

Ele compreende um conjunto de sensores inerciais, conhecido como unidade de medição inercial (IMU), juntamente com um processador de navegação.

O processador de navegação integra as saídas da IMU para fornecer a posição, velocidade e atitude.

Os giroscópios medem a taxa angular, que é usada pelo processador de navegação para manter a solução de atitude do INS. Os acelerômetros, por outro lado, medem a força específica, que é a aceleração devida a todas as forças, exceto a gravidade. Os acelerômetros são alinhados com o corpo de navegação, de modo que a solução de atitude é usada para transformar a medição da força específica no sistema de coordenadas de resolução usado pelo processador de navegação. Um modelo gravitacional é então usado para obter a aceleração da força específica usando a solução de posição. A integração da aceleração produz a solução de velocidade, e a integração da velocidade fornece a solução de posição. A posição e a velocidade para todos os INS e o rumo para sistemas de nível inferior devem ser inicializados antes que o INS possa calcular uma solução de navegação.

Os projetos de giroscópios se dividem em três categorias principais: giroscópios de massa giratória, giroscópios ópticos, incluindo giroscópios de laser em anel (RLGs) e giroscópios de fibra óptica interferométrica (IFOGs), e giroscópios vibratórios. A tecnologia de acelerômetros compreende acelerômetros pendulares e de feixe vibratório. Giroscópios e acelerômetros fabricados com tecnologia de sistemas microeletromecânicos (MEMS) oferecem as vantagens de baixo custo, tamanho e massa, além de alta tolerância a choques, mas apresentam desempenho relativamente baixo.

Os erros em uma solução de navegação inercial aumentam com o tempo, à medida que erros sucessivos do acelerômetro e do giroscópio são somados.

O feedback através do modelo gravitacional atua para estabilizar a posição horizontal e a velocidade, mas desestabiliza o canal vertical. O desempenho geral da navegação pode variar em várias ordens de magnitude, dependendo da qualidade dos sensores inerciais.

### 1.3 Radio and Satellite Navigation

### 1.3.1 Terrestrial Radio Navigation

Esses sistemas de navegação não oferecem a mesma cobertura ou precisão que o GNSS e se limitam a fornecer apenas a posição horizontal. No entanto, eles fornecem um auxílio útil ao GNSS para aplicações críticas de segurança.

Os desenvolvimentos atuais em tecnologia de radionavegação terrestre concentram-se em áreas urbanas, onde o desempenho do GNSS pode ser insatisfatório. O posicionamento por meio de telefones celulares e redes locais sem fio (WLAN) já está consolidado, enquanto técnicas baseadas em transmissões de TV e rádio e comunicações de banda ultralarga (UWB) foram prototipadas.

### 1.3.2 Satellite Navigation

As principais vantagens do GNSS são a alta precisão de posicionamento a longo prazo e o baixo custo do equipamento para o usuário. A principal limitação da navegação por satélite é a falta de continuidade do sinal. Os sinais GNSS são vulneráveis a interferências, tanto acidentais quanto intencionais. Eles também podem ser bloqueados, atenuados e refletidos por edifícios, terrenos e vegetação.radial de 1,0–3,9 m no plano horizontal e 1,6–6,3 m no eixo vertical, dependendo do serviço, do projeto do receptor e da geometria do sinal.

### 1.4 Feature Matching

As técnicas de correspondência de características determinam a posição do usuário comparando características do terreno ou ambiente com um banco de dados, da mesma forma que uma pessoa compararia pontos de referência com um mapa ou um conjunto de direções.

Técnicas de correspondência de mapas utilizam o fato de que veículos terrestres geralmente trafegam em estradas ou trilhos e pedestres não atravessam paredes para restringir o desvio de uma solução de estimativa e/ou corrigir erros em uma medição de posicionamento. Elas acompanham a solução de navegação em um mapa e aplicam correções onde ela se desvia das áreas permitidas.

### 1.5 The Complete Navigation System

Para a maioria das aplicações de navegação pessoal, veículos rodoviários e rastreamento de ativos, os principais fatores são custo, tamanho, peso e consumo de energia. Consequentemente, diferentes combinações de sensores de navegação são adequadas para diferentes aplicações.

Os sistemas de fixação de posição e de estimativa têm características de erro muito diferentes, portanto, para muitas aplicações, um sistema de estimativa, como o INS, é integrado
com um ou mais sistemas de fixação de posição, como o GNSS.

O sistema de estimativa fornece a solução de navegação integrada, pois opera continuamente, enquanto as medições do sistema de fixação de posição são usadas por um algoritmo de estimativa para aplicar correções à solução de navegação do sistema de estimativa.

# PARTE 2- Navigation Mathematics

## Capítulo 2- Coordinate Frames, Kinematics, and the Earth

### 2.1 Coordinate Frames

Para navegação a rotação da Terra tem um impacto significativo no cálculo da navegação.

Sensores inerciais medem seu movimento em relação a um referencial inercial. O GPS mede a posição e a velocidade da antena de um receptor em relação a uma constelação de satélites. No entanto, o usuário deseja saber sua posição em relação à Terra.

Assim, para uma navegação precisa, a relação entre os diferentes sistemas de coordenadas deve ser modelada adequadamente. Adota-se aqui uma convenção de usar letras gregas para denotar sistemas de coordenadas genéricos e letras romanas para denotar sistemas específicos.
Convenção de Nomenclatura para Sistemas de Coordenadas

**Convenção de Nomenclatura para Sistemas de Coordenadas**

O que o trecho quer dizer é o seguinte:

Letras Gregas (α, β, γ, δ, etc.): São usadas para denotar sistemas de coordenadas GENÉRICOS ou ARBITRÁRIOS.

* Quando o texto fala sobre "um quadro α" ou "o quadro β", ele está se referindo a qualquer sistema de coordenadas sem nomeá-lo especificamente. É como usar uma variável x em matemática: ela pode representar qualquer número.

* Isso é útil em discussões teóricas ou quando se está derivando equações que se aplicam a qualquer par de referenciais, independentemente de serem ECI, ECEF, etc.

Letras Romanas (ECI, ECEF, Body, Local, etc.): São usadas para denotar sistemas de coordenadas ESPECÍFICOS e BEM DEFINIDOS.

* ECI (Earth-Centered Inertial)

* ECEF (Earth-Centered, Earth-Fixed)

* Body (Referencial do Objeto/Corpo)

* Local (Referencial de Navegação Local)

Esses são sistemas de coordenadas com características e usos muito particulares, como os que discutimos anteriormente.

Exemplo para Clarificar

Pense em uma aula de física:

* Se o professor está explicando uma lei geral de movimento, ele pode dizer: "A força agindo sobre um objeto no referencial α pode ser calculada...". Aqui, α é um referencial genérico.

* Mais tarde, ao aplicar isso a um problema prático, ele pode dizer: "Vamos calcular a trajetória do satélite no referencial ECI". Aqui, ECI é um referencial específico.
    
Um sistema de coordenadas pode ser definido de duas maneiras. Ele fornece uma origem e um conjunto de eixos em termos dos quais o movimento dos objetos pode ser descrito.

Ele também define a posição e a orientação de um objeto. As duas definições são intercambiáveis. Em um problema de dois quadros, definir qual é o quadro do objeto e qual é o quadro de referência é arbitrário. É igualmente válido para descrever a posição e orientação do quadro α em relação ao quadro β como para descrever quadro  β em relação ao quadro α. Este é um princípio da relatividade: as leis da física parecem as mesmas para todos os observadores. Em outras palavras, descrever a posição de uma estrada em relação a um carro transmite a mesma informação que a posição do carro em relação à estrada.

Um sistema de coordenadas ortogonais tem seis graus de liberdade, a posição da origem, o, e a orientação dos eixos, x, y e z.

Qualquer problema de navegação envolve, portanto, pelo menos dois quadros de coordenadas: um quadro de objeto e um quadro de referência.

O referencial do objeto descreve o corpo cuja posição e/ou orientação é desejada, enquanto o referencial descreve um corpo conhecido, como a Terra, em relação ao qual a posição e/ou orientação do objeto é desejada. Muitos problemas de navegação envolvem mais de um referencial ou até mesmo mais de um referencial de objeto.

O referencial conhecido (ou de referência) é o espaço ou o sistema de coordenadas de base em relação ao qual a posição e/ou orientação do referencial do objeto são definidas.

Nós usamos as coordenadas dentro desse referencial conhecido para especificar onde o objeto está e como ele está orientado.

Referenciais: Objeto vs. Conhecido:

* Referencial do Objeto: É o sistema de coordenadas acoplado ao corpo cuja posição e/ou orientação você quer determinar. Pense em um avião, um satélite ou até mesmo um carro. O referencial do objeto se move junto com ele.

* Referencial Conhecido (ou de Referência): Este é um sistema de coordenadas que serve como ponto de comparação. Geralmente, é um corpo cuja posição e orientação são bem estabelecidas e conhecidas, como a Terra. Ao descrever a posição de um objeto, você o faz em relação a este referencial conhecido.

Exemplo: Se você quer saber onde está um carro, o carro é o "objeto" e a Terra (ou um mapa da Terra) é o "referencial conhecido". Você diria que o carro está a X quilômetros ao norte e Y quilômetros ao leste de um ponto de referência na Terra.

Múltiplos Referenciais na Navegação

Problemas de navegação são complexos porque muitas vezes envolvem mais de um referencial e, por vezes, até mais de um referencial de objeto.

Exemplo: Imagine um avião (referencial de objeto 1) voando em relação à Terra (referencial conhecido). Dentro do avião, pode haver um drone (referencial de objeto 2) que se move em relação ao avião. Para rastrear o drone, você precisaria de informações tanto em relação ao avião quanto em relação à Terra.

Quaisquer dois sistemas de coordenadas podem ter qualquer posição e atitude relativa. 

* Posição Relativa: A origem de um quadro pode estar em qualquer posição em relação à origem do outro quadro. Por exemplo, o quadro A pode estar 10 metros à frente, 5 metros à direita e 2 metros acima do quadro B.

* Atitude Relativa (Orientação): Um quadro pode ter qualquer orientação (rotação) em relação ao outro quadro. Por exemplo, o eixo X do quadro A pode estar apontando para onde o eixo Y do quadro B aponta, e assim por diante. Não há restrições sobre como um quadro pode estar rotacionado ou deslocado em relação ao outro.

Eles também podem ter qualquer velocidade relativa, aceleração, rotação   e assim por diante. A orientação de um quadro em relação a outro é um conjunto único de números, embora haja mais de uma maneira de representar a atitude. No entanto, as outras grandezas cinemáticas não o são. Elas compreendem vetores, que podem ser decompostos em componentes ao longo de quaisquer três eixos mutuamente perpendiculares.Por exemplo, a posição do quadro α em relação ao quadro β pode ser descrita usando os eixos do quadro α, os eixos do quadro β ou os eixos de um terceiro quadro γ. O restante desta seção define os principais sistemas de coordenadas usados em problemas de navegação: o sistema inercial centrado na Terra (ECI), o sistema fixo centrado na Terra (ECEF), a navegação local e o sistema corporal.


**A Relação Cinemática entre Dois Quadros**

Quando falamos de dois sistemas de coordenadas (ou "quadros", como o texto chama, por exemplo, o quadro A e o quadro B), não estamos interessados apenas em onde eles estão (posição) e como estão alinhados (orientação ou atitude). Também nos preocupamos com como eles se movem um em relação ao outro. É aí que entram as grandezas cinemáticas.

**Quando falamos da velocidade de um quadro, na verdade, estamos nos referindo à velocidade do referencial ao qual esse quadro está rigidamente acoplado.**

Relação entre Sistemas de Coordenadas: Posição, Atitude e Outras Grandezas Cinemáticas

O trecho destaca que dois sistemas de coordenadas quaisquer podem ter uma relação relativa complexa:

Para descrever a relação entre dois sistemas de coordenadas (digamos, um sistema 'A' e um sistema 'B'), precisamos de dois tipos principais de informação:

* Posição Relativa: Onde a origem de um sistema está em relação à origem do outro.

* Atitude (Orientação) Relativa: Como os eixos de um sistema estão rotacionados em relação aos eixos do outro.

Além disso, para descrever o movimento de um sistema em relação ao outro, precisamos das grandezas cinemáticas, como velocidade, aceleração e rotação.

1. Velocidade Relativa e Aceleração Relativa

O trecho começa dizendo: "Eles também podem ter qualquer velocidade relativa, aceleração, rotação e assim por diante."

Isso significa que o quadro B pode estar se movendo em relação ao quadro A com:

* Qualquer velocidade linear: O quadro B pode estar se afastando, se aproximando, ou se movendo lateralmente em relação ao quadro A, e essa velocidade pode ser constante ou variar.

* Qualquer aceleração linear: A velocidade do quadro B em relação ao quadro A pode estar aumentando, diminuindo ou mudando de direção.

Essas grandezas são vetoriais, o que significa que elas têm magnitude (intensidade) e direção.

2. Rotação Relativa (Velocidade Angular)

A "rotação" mencionada aqui se refere à velocidade angular. O quadro B pode estar girando em relação ao quadro A, e essa rotação pode ser lenta, rápida, constante ou variável. Assim como a velocidade e a aceleração lineares, a velocidade angular também é uma grandeza vetorial.

Entendi! Você quer uma explicação detalhada sobre a parte que diferencia a orientação (atitude) de outras grandezas cinemáticas como velocidade, aceleração e rotação, no contexto da relação entre sistemas de coordenadas.

A Relação Cinemática entre Dois Quadros

Quando falamos de dois sistemas de coordenadas (ou "quadros", como o texto chama, por exemplo, o quadro A e o quadro B), não estamos interessados apenas em onde eles estão (posição) e como estão alinhados (orientação ou atitude). Também nos preocupamos com como eles se movem um em relação ao outro. É aí que entram as grandezas cinemáticas.

1. Velocidade Relativa e Aceleração Relativa

O trecho começa dizendo: "Eles também podem ter qualquer velocidade relativa, aceleração, rotação e assim por diante."

Isso significa que o quadro B pode estar se movendo em relação ao quadro A com:

    Qualquer velocidade linear: O quadro B pode estar se afastando, se aproximando, ou se movendo lateralmente em relação ao quadro A, e essa velocidade pode ser constante ou variar.

    Qualquer aceleração linear: A velocidade do quadro B em relação ao quadro A pode estar aumentando, diminuindo ou mudando de direção.

Essas grandezas são vetoriais, o que significa que elas têm magnitude (intensidade) e direção.

2. Rotação Relativa (Velocidade Angular)

A "rotação" mencionada aqui se refere à velocidade angular. O quadro B pode estar girando em relação ao quadro A, e essa rotação pode ser lenta, rápida, constante ou variável. Assim como a velocidade e a aceleração lineares, a velocidade angular também é uma grandeza vetorial.

**A Diferença Fundamental: Orientação vs. Outras Grandezas Cinemáticas**

Aqui chegamos ao cerne da sua pergunta, a distinção crucial que o texto faz:

"A orientação de um quadro em relação a outro é um conjunto único de números, embora haja mais de uma maneira de representar a atitude. No entanto, as outras grandezas cinemáticas não o são."

Vamos analisar isso em profundidade:

Orientação (Atitude) - Um "Conjunto Único de Números"

* O que é: A orientação (ou atitude) descreve a configuração rotacional de um quadro em relação a outro. É como o "alinhamento" dos eixos de um quadro em relação aos eixos do outro.

* Por que é única: Uma vez que você define como o quadro B está rotacionado em relação ao quadro A, essa descrição é completa e não ambígua. Há apenas uma forma física de como eles podem estar alinhados.

* Exemplo: Se você disser que o eixo X do quadro B está alinhado com o eixo Y do quadro A, o eixo Y do quadro B com o eixo -X do quadro A, e o eixo Z do quadro B com o eixo Z do quadro A, isso descreve uma rotação específica de 90 graus em torno do eixo Z. Essa é uma rotação única.

"Mais de uma maneira de representar": Embora a rotação física seja única, existem diferentes ferramentas matemáticas para descrever essa rotação:

* Matrizes de Rotação (ou Matrizes de Cossenos Diretores): Uma matriz 3x3 que transforma as coordenadas de um vetor de um quadro para o outro. É muito rigorosa e fundamental.

* Ângulos de Euler: Uma sequência de três rotações sucessivas em torno de eixos específicos (por exemplo, "yaw", "pitch", "roll" para aviões). São intuitivos, mas podem ter problemas em certas configurações (como o "gimbal lock").

* Quaternions: Uma representação compacta de quatro números que é eficiente computacionalmente e evita problemas como o "gimbal lock".

Independentemente da ferramenta que você usa (matriz, ângulos de Euler, quaternion), todas elas apontam para a mesma e única configuração rotacional entre os dois quadros. Você pode converter entre essas representações sem perder informação.

Outras Grandezas Cinemáticas (Velocidade, Aceleração, Rotação) - "Não o são" (não são um conjunto único de números sem um referencial definido)

* O que são: Essas grandezas descrevem o movimento ou a mudança de movimento de um quadro em relação ao outro.

* Por que não são "únicas" sem um referencial: Ao contrário da atitude, que descreve uma relação entre os eixos, a representação numérica da velocidade, aceleração ou velocidade angular depende do sistema de coordenadas em que elas são expressas (projetadas).

* Exemplo da Velocidade: Imagine um carro (quadro B) se movendo em uma estrada (quadro A).

A velocidade do carro em relação à estrada é um vetor físico.

Se você expressar os componentes desse vetor usando os eixos do carro (frente, lado, cima), você terá valores como (X km/h para frente, Y km/h para o lado, Z km/h para cima).

Se você expressar os componentes desse mesmo vetor usando os eixos da estrada (Norte, Leste, Cima), você terá valores diferentes, como (N km/h para o Norte, L km/h para o Leste, C km/h para cima).

O vetor físico de velocidade é o mesmo, mas seus componentes numéricos mudam dependendo de qual conjunto de eixos você usa para "medir" ou "decompor" esse vetor.

O mesmo vale para a aceleração e a velocidade angular. Um objeto pode estar girando no espaço. A descrição dessa rotação (sua velocidade angular) será um vetor com diferentes componentes dependendo se você a projeta nos eixos do próprio objeto ou nos eixos de um referencial fixo no espaço.


A rotação relativa nos diz como os eixos do Quadro B estão alinhados em relação aos eixos do Quadro A. É como se você estivesse tentando descrever a "atitude" ou "postura" de um objeto em relação a outro.

atitude é sinônimo de rotação relativa quando falamos da relação entre sistemas de coordenadas.

### 2.1.1 Earth-Centered Inertial Frame

Em física, um sistema de coordenadas inercial é aquele que não acelera nem gira em relação ao resto do Universo.

Quando o texto diz que um sistema de coordenadas inercial é aquele que "não acelera nem gira em relação ao resto do Universo", ele está, de certa forma, descrevendo-o como um sistema estático ou não-acelerado.

O Que Isso Significa na Prática

* "Não acelera": Significa que a origem do sistema de coordenadas inercial não está ganhando ou perdendo velocidade, nem mudando de direção em seu movimento. Ela se move com velocidade constante ou está em repouso.

* "Nem gira": Significa que os eixos do sistema de coordenadas inercial (X, Y, Z) não estão girando. Eles apontam sempre para as mesmas direções fixas no "espaço distante" (geralmente em relação a estrelas muito distantes, que são consideradas fixas).


Quando se diz que os eixos de um sistema inercial não estão girando, não significa que eles não estão girando em torno de si mesmos (essa ideia nem faria muito sentido para um eixo, que é uma linha).

Significa, sim, que eles não estão mudando a direção em que apontam no espaço.

Imagine o seguinte:

* Eixos que não giram (inercial): Pense nos eixos X, Y e Z de um sistema inercial como apontando para estrelas fixas muito, muito distantes. Não importa onde o observador ou o objeto esteja se movendo nesse sistema, esses eixos continuam apontando para as mesmas estrelas. A direção deles no universo é constante.

* Eixos que giram (não inercial, como o ECEF da Terra): Os eixos do sistema ECEF (fixo na Terra) giram junto com a Terra. O eixo X, por exemplo, sempre aponta para o meridiano de Greenwich no equador. Mas como a Terra está girando, essa direção no espaço sideral está mudando constantemente.

Então, você está absolutamente certo: "não girar" para os eixos significa que eles mantêm uma orientação constante no espaço absoluto, ou seja, a direção para a qual eles apontam não muda ao longo do tempo.

A aceleração descreve a taxa de mudança da velocidade de um objeto. A velocidade descreve o quão rápido um objeto está se movendo e em qual direção. E ambas são grandezas vetoriais.

1. Rotação (do Sistema de Coordenadas)

Quando falamos que um sistema de coordenadas não tem rotação, isso se refere a:

* A direção para a qual seus eixos apontam permanece fixa no espaço. Imagine os eixos X, Y e Z desse sistema. Eles sempre apontarão para as mesmas estrelas distantes, por exemplo. Eles não mudam de "orientação" no espaço.

* Isso não tem a ver com os eixos girarem sobre si mesmos, mas sim com o alinhamento global do conjunto de eixos.

2. Velocidade Angular

A velocidade angular de um sistema de coordenadas está diretamente relacionada a essa "rotação" que acabamos de descrever:

* É a taxa de mudança da orientação (atitude) do sistema de coordenadas ao longo do tempo. Se um sistema de coordenadas está girando (ou seja, seus eixos estão mudando a direção para a qual apontam), ele tem uma velocidade angular.

* Se os eixos de um sistema de coordenadas estão fixos no espaço (não mudam de direção), sua velocidade angular é zero.

eixos do referencial ECI. A rotação mostrada é a da Terra em relação ao espaço. O eixo z sempre aponta ao longo do eixo de rotação da Terra, do centro para o polo norte (verdadeiro, não magnético). Os eixos x e y estão dentro do plano equatorial. Eles não giram com a Terra, mas o eixo y sempre está 90 graus à frente do eixo x na direção de rotação. Isso não define exclusivamente o sistema de coordenadas; também é necessário especificar o instante em que os eixos do sistema de coordenadas inerciais coincidem com os do sistema ECEF

O ECI: Um Observador "De Fora" da Terra

Imagine que você é um observador muito, muito distante no espaço, olhando para a Terra. Para você, as estrelas distantes parecem fixas.

Eixo Z do ECI:

* "O eixo z sempre aponta ao longo do eixo de rotação da Terra, do centro para o polo norte (verdadeiro, não magnético)."

* Este eixo Z é o mais fácil de entender. Ele está alinhado com o eixo de rotação da Terra. Como o eixo de rotação da Terra aponta para uma direção fixa no espaço (próximo à Estrela Polar, por exemplo), o eixo Z do ECI também aponta para essa direção fixa no espaço. Ele não "gira" no sentido de mudar sua direção para onde aponta.

Eixos X e Y do ECI:

* "Os eixos x e y estão dentro do plano equatorial. Eles não giram com a Terra..."

* Esta é a parte chave. Pense novamente no observador distante. Enquanto a Terra gira, o ECI mantém seus eixos X e Y apontando para direções fixas no espaço, no plano do equador da Terra.

Exemplo: Imagine que, em um certo momento, o eixo X do ECI aponta para uma estrela específica. Mesmo que a Terra gire 360 graus em 24 horas, o eixo X do ECI continua apontando para aquela mesma estrela. Ele não se move junto com o ponto na superfície da Terra que estava alinhado com ele inicialmente.

A Diferença entre ECI e ECEF

Para entender melhor, compare com o Referencial ECEF (Earth-Centered, Earth-Fixed):

* ECEF: Este sistema gira junto com a Terra. O eixo X do ECEF, por exemplo, está sempre fixo no meridiano de Greenwich no equador. Como a Terra gira, o eixo X do ECEF muda constantemente sua direção no espaço (ele "varre" o espaço junto com a Terra).

* ECI: Este sistema NÃO gira com a Terra. Seus eixos X e Y mantêm uma orientação fixa no espaço, mesmo que a Terra esteja girando "por baixo" deles. O eixo Z também é fixo no espaço.

"Mas o eixo y sempre está 90 graus à frente do eixo x na direção de rotação."

Este trecho pode ser um pouco confuso. O que ele quer dizer é que, dentro do próprio sistema ECI, os eixos X, Y e Z formam um sistema de coordenadas cartesiano padrão (ortogonais entre si). O "90 graus à frente" apenas descreve a relação espacial entre X e Y dentro do ECI, consistente com a regra da mão direita, e como eles se relacionam com a direção de rotação da Terra, mesmo que eles próprios não estejam girando.

"Isso não define exclusivamente o sistema de coordenadas; também é necessário especificar o instante em que os eixos do sistema de coordenadas inerciais coincidem com os do sistema ECEF."

Esta frase é importante. Ela significa que:

* A definição de "não girar" e "eixo Z alinhado com a rotação da Terra" não é suficiente para fixar a posição dos eixos X e Y do ECI no espaço.

* Pense que você pode ter infinitos sistemas ECI. Todos teriam o eixo Z apontando para o polo norte, e seus eixos X e Y estariam no plano equatorial e não girariam. Mas onde exatamente o eixo X aponta no plano equatorial? Para uma estrela específica? Para o ponto do equador que estava alinhado com Greenwich em 1º de janeiro de 2000?

* Para fixar um ECI específico, você precisa de um momento de referência. Por exemplo, você pode definir que, no dia 1º de janeiro de 2000, às 00:00:00 UTC, o eixo X do seu ECI estava perfeitamente alinhado com o eixo X do ECEF (que aponta para Greenwich). A partir desse momento, o ECI mantém essa orientação fixa no espaço, enquanto o ECEF continua girando com a Terra.A outra opção, usada pela comunidade científica, é definir o eixo x como a direção da Terra ao Sol no equinócio de primavera, que é o equinócio de primavera no hemisfério norte. Esta é a mesma direção do centro da Terra até a intersecção do plano equatorial da Terra com o plano orbital Terra-Sol (eclíptica).

O Problema do Movimento Polar

Quando definimos o eixo Z do referencial ECEF (Fixo Centrado na Terra) ou do ECI (Inercial Centrado na Terra), dissemos que ele aponta para o Polo Norte. Mas a realidade é um pouco mais complexa:

* O eixo de rotação da Terra não é fixo em relação à própria Terra sólida. Imagine um pião girando; o ponto onde ele toca o chão pode "dançar" um pouco. Algo semelhante acontece com a Terra. O eixo em torno do qual a Terra gira realmente se move um pouco em relação à sua crosta terrestre (a "Terra sólida").

* "Polos seguindo aproximadamente uma trajetória circular de raio de 15 m": Isso significa que o ponto exato onde o eixo de rotação da Terra "fura" a superfície (o Polo Geográfico) não é estático. Ele se desloca, descrevendo uma pequena trajetória quase circular, com um raio de cerca de 15 metros.

Esse movimento, embora pequeno (15 metros é muito pouco em comparação com o raio da Terra), é significativo para aplicações que exigem alta precisão, como navegação de satélites, geodesia (ciência da forma e gravidade da Terra) e astronomia. Se você assume que o polo é fixo e ele não é, seus cálculos de posição e orientação terão um erro.

A Solução: Polos de Referência Convencionais

Para lidar com essa imprecisão, a comunidade científica (representada pelo IERS - International Earth Rotation and Reference Systems Service) adotou polos de referência convencionais:

* Polo de Referência IERS (IRP) / Polo Terrestre Convencional (CTP): Em vez de tentar rastrear o polo "verdadeiro" que se move, foi definida uma posição média fixa para o Polo Norte. Essa posição foi estabelecida com base na média da posição do polo entre os anos de 1900 e 1905.

* Por que isso ajuda? Ao usar um ponto de referência fixo e acordado internacionalmente, todos os cálculos geodésicos e de navegação podem usar a mesma base, garantindo consistência e precisão. É uma convenção para padronizar as medições.

O Sistema de Referência Inercial Convencional (CIRS)

Com base nessa ideia de um polo de referência fixo, foi definido um sistema inercial ainda mais preciso e padronizado:

* Origem: O centro de massa da Terra.

* Eixo Z: Alinhado com o IRP/CTP (o polo norte de referência fixo).

* Eixo X: É definido com base no eixo Terra-Sol no equinócio vernal (de primavera). O equinócio vernal é um ponto específico na órbita da Terra onde o plano do equador terrestre cruza o plano da órbita da Terra ao redor do Sol. Historicamente, este ponto é usado como uma referência para sistemas inerciais astronômicos.

* Eixo Y: É definido para completar um sistema de coordenadas ortogonal de mão direita (normalmente 90 graus à frente do eixo X no plano equatorial).

O CIRS (Conventional International Terrestrial Reference System) é, portanto, uma implementação padronizada e altamente precisa de um sistema de coordenadas inercial. Ele foi projetado para oferecer a maior precisão possível para aplicações que não podem tolerar os pequenos movimentos do eixo de rotação real da Terra


### 2.1.2 Earth-Centered Earth-Fixed Frame

Todos os eixos permanecem fixos em relação à Terra.

O referencial ECEF é denotado pelo símbolo e e tem sua origem no centro do elipsoide que modela a superfície da Terra, que está aproximadamente no centro de massa.

O quadro ECEF usando o IRP/CTP e o IRM/CZM também é conhecido como sistema de referência terrestre convencional (CTRS), e alguns autores usam o símbolo t para denotá-lo

**Analogia Simples**

Imagine uma bússola de navio (giroscópica) e um mapa-múndi giratório:

* ECI: É como a agulha de uma bússola giroscópica que sempre aponta para o Norte verdadeiro (fixo no espaço), independentemente de como o navio (Terra) está girando. Os eixos da bússola estão fixos no espaço.

* ECEF: É como o mapa-múndi giratório. Seus eixos estão presos ao globo. Quando você gira o globo (Terra), os eixos do mapa-múndi giram junto com ele em relação ao ambiente (espaço).

A grande diferença é:

* ECI: Os eixos NÃO giram em relação ao espaço.

* ECEF: Os eixos GIRAM em relação ao espaço (porque estão fixos na Terra que gira).

### 2.1.3 Local Navigation Frame

O quadro de navegação local, quadro de navegação de nível local, geodésico ou quadro geográfico é denotado pelo símbolo n (alguns autores usam g). Sua origem é o ponto para o qual uma solução de navegação é buscada (ou seja, o sistema de navegação, o usuário ou o centro de massa do veículo hospedeiro).

É um sistema de coordenadas muito utilizado em navegação e robótica por ser altamente intuitivo para descrever o movimento e a posição de um objeto em uma área geograficamente limitada.

A origem do Local Navigation Frame não é fixa no centro da Terra como o ECI ou o ECEF. Em vez disso, sua origem é definida em um ponto específico na superfície da Terra de interesse para a navegação.

Esse ponto de origem é frequentemente:

* A posição inicial do veículo (por exemplo, onde um carro começou sua jornada ou onde um drone decolou).

* Um ponto de referência fixo conhecido (como um aeroporto para uma aeronave ou um canto de uma sala para um robô interno).

O eixo z, também conhecido como eixo descendente (D), é definido como a normal à superfície do elipsoide de referência (Seção 2.3.1), apontando aproximadamente para o centro da Terra.Modelos de gravidade simples assumem que o vetor de gravidade coincide com o eixo z do quadro de navegação local. A gravidade real se desvia ligeiramente desse valor devido a anomalias locais. O eixo x, ou eixo norte (N), é a projeção no plano ortogonal ao eixo z da reta que vai do usuário ao polo norte. Ao completar o conjunto ortogonal, o eixo y sempre aponta para o leste e, portanto, é conhecido como eixo leste (E).

### 2.1.4 Body Frame

O body Frame, às vezes conhecida como estrutura do veículo, compreende a origem e a orientação do objeto para o qual uma solução de navegação é buscada.A origem é coincidente com a do quadro de navegação local, mas os eixos permanecem fixos em relação ao corpo e são geralmente definidos como x = para frente (ou seja, a direção usual de deslocamento), z = para baixo (ou seja, a direção usual da gravidade) e y = direita, completando o conjunto ortogonal. Para movimento angular, o eixo x é o eixo de rotação, o eixo y é o eixo de inclinação e o eixo z é o eixo de guinada.

Todos os sensores inerciais de fixação medem o movimento da estrutura do corpo (em relação a uma estrutura inercial genérica).

1. Sensores Inerciais de Fixação (Strapdown Inertial Sensors)

"Sensores inerciais de fixação" refere-se ao tipo de sensor inercial mais comum e acessível hoje em dia, encontrado em smartphones, drones, carros, etc. Eles são "fixos" (strapdown) ao corpo ou plataforma em que estão instalados.

* Contraste com plataformas estabilizadas: Antigamente, alguns sistemas inerciais usavam plataformas gimbal estabilizadas. Os sensores ficavam em uma plataforma que era ativamente mantida em uma orientação fixa no espaço, compensando a rotação do veículo. Isso era complexo e caro. Os sistemas "strapdown" são mais simples mecanicamente porque os sensores estão diretamente fixados ao corpo que está se movendo e girando.

2. Medem o Movimento da Estrutura do Corpo (Body Frame)

Como os sensores estão fixos no corpo, eles medem o movimento desse corpo em particular.

* Acelerômetros: Medem a aceleração linear do ponto onde estão localizados no corpo. Se o corpo acelera para frente, o acelerômetro sente essa aceleração na direção "para frente" do corpo.

* Giroscópios: Medem a velocidade angular (rotação) do corpo em torno dos seus próprios eixos. Se o corpo está girando para a direita, o giroscópio sente essa rotação.

Em outras palavras, as leituras brutas desses sensores estão sempre no referencial do objeto (o Body Frame). Eles te dizem "como eu estou me movendo", não "como eu estou me movendo em relação à Terra" ainda.

3. Em Relação a uma Estrutura Inercial Genérica

Esta é a parte crucial e um pouco abstrata:

* Os princípios da física que governam o funcionamento dos acelerômetros e giroscópios (como as Leis de Newton e os efeitos da inércia) são mais simples e válidos em um referencial inercial.

* Quando um acelerômetro mede uma aceleração, ele o faz em relação a esse "espaço inercial" ou "estrutura inercial genérica". Pense nesse referencial inercial como um pano de fundo cósmico onde não há aceleração nem rotação.

* É nesse "espaço" que o sensor detecta a inércia do movimento do corpo ao qual está preso. Por exemplo, se o corpo acelera, o sensor "sente" essa aceleração porque está mudando sua velocidade em relação a esse referencial inercial.

O símbolo b é usado para denotar a estrutura do corpo do objeto primário de interesse. No entanto, muitos problemas de navegação envolvem múltiplos objetos, cada um com sua própria estrutura corporal, para os quais símbolos alternativos, como s para um satélite e a para uma antena, devem ser usados.

### 2.1.5 Other Frames

#### geocentric frame,

O referencial geocêntrico, denotado por c, é semelhante ao referencial de navegação local, exceto que o eixo z aponta da origem para o centro da Terra. O eixo x é, novamente, a projeção da reta até o polo norte no plano ortogonal ao eixo z.

O referencial do plano tangente, t, também é conhecido como referencial geodésico local. É semelhante ao referencial de navegação local, exceto que a origem não coincide com o objeto de navegação, mas sim é fixa em relação à Terra. Este quadro é usado para navegação em uma área localizada, como pouso de aeronaves.

#### wander azimuth frame w (alguns autores usam n)

A origem e o eixo z são coincidentes com os do quadro de navegação local.

1. Alinhamento Nominal (Ideal)

"Na maioria dos sistemas, os eixos sensíveis dos instrumentos inerciais são nominalmente alinhados com os eixos da estrutura do corpo..."

* Eixos Sensíveis do Instrumento: Cada acelerômetro e giroscópio tem seus próprios eixos de medição internos. Por exemplo, um acelerômetro de três eixos tem um eixo sensível para X, um para Y e um para Z.

* Estrutura do Corpo (Body Frame): É o sistema de coordenadas de referência do objeto onde a IMU está instalada (por exemplo, o chassi de um drone, a fuselagem de um avião).

* Alinhamento Nominal: No projeto e fabricação, a intenção é que os eixos de medição do sensor (os "eixos sensíveis") fiquem perfeitamente alinhados com os eixos definidos para a estrutura do corpo. Se o eixo X do seu drone aponta para frente, espera-se que o eixo X do acelerômetro também aponte exatamente para frente.

2. O Desvio (Misalignment)

"...mas sempre haverá algum desvio."

* Realidade da Fabricação: Na prática, é impossível atingir um alinhamento perfeito devido a tolerâncias de fabricação, montagem, temperatura e outros fatores. Sempre haverá um pequeno desvio angular (um desalinhamento minúsculo) entre os eixos sensíveis do instrumento e os eixos ideais da estrutura do corpo.

* Impacto: Mesmo um desvio de frações de grau pode introduzir erros significativos nos cálculos de navegação, especialmente em aplicações de alta precisão ou ao longo do tempo. Se você assume que o eixo X do acelerômetro está perfeitamente alinhado com o eixo X do seu drone, mas ele está um pouco torto, todas as suas medições de aceleração nesse eixo serão ligeiramente projetadas nas outras direções.

3. A Preferência por Tratar como Estruturas Separadas

"Portanto, alguns autores preferem tratar esses eixos sensíveis como estruturas separadas de instrumentos inerciais, com uma estrutura de coordenadas para cada acelerômetro e giroscópio."

* Abordagem Simplificada (Comum em Muitas Aplicações): Para muitos sistemas (como em smartphones ou drones amadores), assume-se que o desvio é negligenciável ou que ele já foi calibrado (corrigido) no firmware do sensor. Então, você simplesmente trata a IMU como um todo, com seus eixos já alinhados ao Body Frame do dispositivo.

* Abordagem de Alta Precisão (A preferência de alguns autores): Em sistemas onde a precisão é crítica (por exemplo, navegação de mísseis, exploração espacial, drones profissionais de mapeamento), os engenheiros e pesquisadores não podem se dar ao luxo de ignorar esses pequenos desvios. Eles podem modelar cada sensor individualmente:

* Cada sensor tem seu próprio "quadro de instrumento": Um acelerômetro X teria seu próprio quadro, o acelerômetro Y outro, e assim por diante para cada giroscópio.

* Matrizes de Alinhamento: Seriam calculadas pequenas matrizes de rotação (ou "matrizes de alinhamento") para cada um desses "quadros de instrumento" que descrevem exatamente como ele está desalinhado em relação ao Body Frame principal.

* Calibração Rigorosa: Essas matrizes seriam determinadas através de um processo de calibração muito rigoroso, onde o sistema é submetido a movimentos controlados e as leituras são comparadas com um referencial de verdade.

* Para sistemas que exigem alta precisão, é fundamental saber e compensar esses pequenos desvios de alinhamento (também chamados de misalignment errors ou installation errors). Ignorá-los resultaria em erros significativos na posição, velocidade e atitude calculadas ao longo do tempo.

Como se Descobre e Compensa Esses Desvios?

O processo de descobrir e compensar esses desvios é chamado de calibração de alinhamento ou calibração de instalação. É uma parte crucial do processo de calibração geral de uma IMU.

Aqui estão as formas mais comuns de fazer isso:

1. Calibração em Mesa de Rotação (Gimbal) de Alta Precisão

* O que é: Esta é a forma mais tradicional e precisa de calibração. A IMU é montada em uma mesa de rotação multi-eixos (com gimbals controlados com precisão).

* Como funciona: A mesa é movida para posições e rotações conhecidas e muito precisas. As leituras da IMU são então comparadas com os valores de referência da mesa. As diferenças entre o que a IMU mede e o que deveria medir (dada a posição e orientação conhecida da mesa) são usadas para calcular os erros de alinhamento (e outros erros, como bias e scale factor).

* Resultado: Uma matriz de calibração (ou uma série de parâmetros) é gerada. Essa matriz descreve o pequeno desalinhamento entre o quadro sensível da IMU e o quadro da mesa (que é um substituto para o Body Frame ideal).

* Uso: Nos cálculos posteriores, cada leitura bruta da IMU é multiplicada por essa matriz de calibração para "corrigir" o desalinhamento, efetivamente rotacionando os dados do quadro real do sensor para o Body Frame nominal.

2. Calibração no Campo / In-situ (com ou sem Referência Externa)

Para IMUs de menor custo ou para sistemas que não podem ser levados para um laboratório com mesas de alta precisão, são usadas técnicas de calibração "no local".

Com Referência Externa (GPS, LiDAR, etc.):

* Ideia: O sistema IMU é integrado com outro sensor que fornece uma referência de posição ou orientação de alta precisão (como um GPS de dupla antena, um sistema LiDAR que mapeia o ambiente, ou até mesmo um sistema de posicionamento óptico).

* Como funciona: O veículo com a IMU a bordo é movido em padrões específicos (por exemplo, voltas, acelerações e desacelerações) enquanto ambos os sensores (IMU e referência externa) coletam dados. Algoritmos de estimação (como Filtros de Kalman estendidos) usam a diferença entre os dados da IMU e os dados de referência para estimar o alinhamento da IMU em relação ao Body Frame do veículo (e, por extensão, em relação à referência externa).

* Vantagem: Pode ser feito no ambiente de operação real.

* Desvantagem: Depende da precisão do sensor de referência e do ambiente de operação.

Sem Referência Externa (Apenas IMU - "Self-Calibration"):

* Ideia: Explora as propriedades conhecidas da gravidade e da rotação da Terra.

* Como funciona: O usuário move a IMU em uma sequência específica de orientações (por exemplo, colocá-la em cada uma das 6 faces de um cubo por um tempo, ou girá-la lentamente). Durante esse movimento, o acelerômetro pode ser usado para determinar a direção da gravidade em diferentes orientações, e o giroscópio pode detectar rotações. Algoritmos processam esses dados para estimar os erros, incluindo o desalinhamento.

* Vantagem: Não requer equipamento externo caro.

* Desvantagem: Geralmente menos preciso que a calibração com mesa de rotação, e pode ser mais sensível a ruído e distúrbios externos.

No entanto, é geralmente mais simples tratar os desvios dos eixos do corpo (ou seja, os desalinhamentos da montagem do instrumento) como um conjunto de perturbações. Algumas IMUs são fabricadas em uma configuração "inclinada", na qual os eixos sensíveis dos sensores não estão alinhados com o invólucro. Neste caso, a estrutura do instrumento inercial deve ser considerada distinta da estrutura do corpo, embora a transformação seja frequentemente realizada dentro da IMU.

1. Modelo de Perturbação: Para a maioria dos casos, pequenos desalinhamentos de fabricação são tratados como erros que são calibrados e corrigidos nos dados de saída. Os dados finais parecem vir de sensores perfeitamente alinhados com o Body Frame.

2. Modelo de Estrutura Distinta (para IMUs Inclinadas): Para designs específicos onde os sensores são intencionalmente montados de forma não ortogonal, a relação entre os eixos do sensor e o invólucro da IMU é uma transformação geométrica fundamental. No entanto, essa transformação é geralmente gerenciada internamente pela própria IMU, entregando dados ao usuário em um formato ortogonal padrão.

Outro problema é que, devido ao tamanho finito dos sensores, a origem de cada sensor será ligeiramente diferente. Antes do cálculo da solução de navegação, as saídas do sensor inercial devem ser transformadas em um ponto de referência comum. Novamente essa transformação geralmente é realizada dentro da IMU. 2 No cálculo do movimento de satélites GNSS, são utilizados referenciais de coordenadas orbitais, denotados por o.

### 2.2 Kinematics

Na navegação, o movimento linear e angular de um sistema de coordenadas deve ser descrito em relação a outro.

Aceleração e velocidade medem o movimento linear, enquanto a taxa de variação dos ângulos dos eixos (ou seja, a velocidade angular) mede o movimento angular. 

Quando falamos de movimento angular de um sistema de coordenadas, estamos falando sobre o quanto ele está girando, ou seja, o quanto a direção de seus eixos está variando no espaço.

O movimento linear de um sistema de coordenadas descreve o quanto a sua origem (o ponto de referência do sistema) está se deslocando no espaço, em linha reta ou curva.

A descrição do movimento seja completa e útil, é sempre necessário especificar qual é o referencial de origem (o "quadro de referência") em relação ao qual o movimento do outro quadro (referencial do objeto) está sendo descrito.

A maioria das grandezas cinemáticas, como posição, velocidade, aceleração e taxa angular, envolvem três sistemas de coordenadas:

* O quadro cujo movimento é descrito, conhecido como quadro do objeto   α
* O quadro ao qual esse movimento se refere, conhecido como quadro de referência β
* O conjunto de eixos em que esse movimento é representado, conhecido como quadro de resolução y

O Quadro de Resolução (γ)

* O quê: Este é o conjunto de eixos em que os valores numéricos (componentes) das grandezas cinemáticas são expressos. É onde os números que representam o vetor são "projetados".

* Para que serve: É onde você "lê" os componentes X, Y, Z do vetor de posição, velocidade ou aceleração. A mesma grandeza física (o mesmo vetor) terá componentes diferentes se for resolvida em quadros diferentes.

Exemplos:

* Você pode querer a velocidade do avião (quadro α) em relação à Terra (quadro de referência β - ECEF), mas expressa nos eixos do próprio avião (quadro de resolução γ - Body Frame do avião). Isso lhe daria a velocidade do ar em termos de "para frente", "para o lado" e "para cima" do avião.

* Ou você pode querer a aceleração do carro (quadro α) em relação à Terra (quadro de referência β - ECEF), mas expressa nos eixos Norte-Leste-Para Baixo da navegação local (quadro de resolução γ - LNF). Isso lhe daria a aceleração em termos de "aceleração para o Norte", "aceleração para o Leste" e "aceleração vertical".

Exemplo Final para Solidificar

Vamos pegar a velocidade.

* Quadro do Objeto (α): O carro.

* Quadro de Referência (β): A superfície da Terra (ou o ECEF).

* Quadro de Resolução (γ):

1. Cenário 1: Se você quer a velocidade do carro em relação à Terra, expressa nos eixos do carro. Aqui, γ=α. Isso é útil para o controle do carro (ex: "estou andando 50 km/h para frente do meu chassi").

2. Cenário 2: Se você quer a velocidade do carro em relação à Terra, expressa nos eixos Norte-Leste-Para Baixo (LNF). Aqui, γ=LNF. Isso é útil para navegação em um mapa (ex: "estou andando 40 km/h para o Norte e 30 km/h para o Leste").

O referencial do objeto, β, e o referencial, α, devem ser diferentes; caso contrário, não há movimento.

Aqui, a seguinte notação é usada para posição cartesiana, velocidade, aceleração e taxa angular: vαβγ​

Onde o vetor, x, descreve uma propriedade cinemática do quadro α em relação ao quadro β, expressa nos eixos do quadro γ. Para a atitude, apenas o quadro do objeto, α, e o quadro de referência, β, estão envolvidos; não há quadro de resolução.

Todos os métodos de representação de atitude cumprem duas funções. Eles descrevem a orientação de um sistema de coordenadas em relação a outro (por exemplo, um sistema de objetos em relação a um sistema de referência). Eles também fornecem um meio de transformar um vetor de um conjunto de eixos de resolução para outro.

Exemplo prático para a segunda função:

Imagine um drone (Quadro do Objeto α) voando, e você tem um vetor de vento medido por um sensor no drone.

* O sensor mede o vetor de vento nas coordenadas do drone (seu Body Frame - Quadro de Resolução γ1​). Por exemplo, o vento está vindo da direita do drone.

* Agora, você quer saber a direção e magnitude desse vento em relação ao Norte e Leste da Terra (Quadro de Resolução γ2​ - o Local Navigation Frame).

O Quadro de Resolução (γ) em um Celular

Em um celular, a IMU interna (acelerômetro, giroscópio e magnetômetro) e os sensores de GPS estão constantemente medindo o movimento e a posição do aparelho. Para que essas informações sejam úteis, elas precisam ser apresentadas em um sistema de coordenadas que faça sentido para o software e para o usuário. Esse sistema de coordenadas é o quadro de resolução.

A beleza do quadro de resolução é que ele pode ser qualquer um dos quadros que estamos usando, dependendo do que o aplicativo precisa. O celular não tem um único quadro de resolução; ele usa o que for mais conveniente no momento.

Aqui estão os principais quadros de resolução usados por um celular e como ele usa cada um:

Exemplos Práticos de Quadros de Resolução em Celulares

1. Quadro de Resolução: O Próprio Celular (Body Frame)

O quê: Os eixos X, Y e Z do próprio celular. O eixo X, por exemplo, pode apontar para a lateral do celular, o Y para cima e o Z para a tela.

Como é usado: Os dados brutos dos sensores da IMU do celular são sempre expressos neste quadro.

* Quando você gira o celular, o giroscópio mede a rotação em relação aos eixos do celular.

* Quando você o sacode para a frente, o acelerômetro mede a aceleração nos eixos do celular.

Função: Este quadro de resolução é crucial para entender o movimento intrínseco do aparelho. Por exemplo, um aplicativo pode usá-lo para detectar gestos como "agitar para desfazer" ou para saber se você está segurando o celular em modo paisagem ou retrato.

2. Quadro de Resolução: O Quadro de Navegação Local (LNF/NED)

O quê: Um quadro alinhado com as direções cardeais (Norte, Leste) e a gravidade (Para Cima/Baixo). A origem pode ser a posição inicial do celular.

Como é usado: Este quadro de resolução é essencial para aplicativos de navegação e realidade aumentada (AR).

* O software do celular pega as leituras dos sensores brutos (no Body Frame) e as transforma para este quadro.

* Uma vez que a aceleração e a velocidade são expressas no LNF, o aplicativo pode dizer, por exemplo: "o celular se moveu 5 metros para o Norte" ou "a aceleração é de 2 m/s² para a Esquerda".

Função: Permite que o software posicione objetos virtuais em um ambiente real (AR) ou mostre sua posição e direção em um mapa de forma coerente.

3. Quadro de Resolução: O Quadro da Tela (Display Frame)

O quê: Um quadro 2D ou 3D que tem seus eixos alinhados com a orientação da tela do celular. O eixo X pode ir da esquerda para a direita da tela, o Y de cima para baixo, etc.

Como é usado: O celular usa esse quadro de resolução para entender a orientação da tela.

* Quando o giroscópio detecta que o celular foi girado para o lado, o sistema operacional usa essa informação para reorientar a tela de retrato para paisagem.

* Jogos de celular que usam a inclinação do aparelho para controlar um personagem (como um avião ou um carro) usam a rotação do Body Frame para determinar a orientação do Display Frame e ajustar os controles.

Função: Gerencia a interface do usuário e as interações baseadas em movimento.

O Papel da Atitude e da Transformação

O celular consegue usar todos esses quadros de resolução de forma transparente graças à atitude (rotação relativa). A IMU e os algoritmos de fusão de sensores estão constantemente calculando a atitude do Body Frame do celular em relação a um referencial de navegação (como o LNF).

Essa informação de atitude (representada como uma matriz de rotação ou um quatérnio) é a "ponte" matemática que permite ao software do celular transformar os dados dos sensores brutos (no quadro de resolução Body Frame) para qualquer outro quadro de resolução que seja necessário (LNF, Display Frame, etc.).

**Definindo atitude, movimento linear e angular**

Conceito Geral: A atitude é um termo genérico que se refere à orientação de um sistema de coordenadas em relação a outro. É a descrição de como um objeto está "virado" no espaço.

O que ela representa: É a rotação que você precisaria aplicar a um sistema de coordenadas de referência (como o Norte, Leste, Para Baixo) para que ele se alinhe com o sistema de coordenadas do objeto (o Body Frame).

* Movimento linear não tem relação com atitude. O movimento linear (velocidade e aceleração) se refere à posição do objeto e como ela muda.

* Movimento angular tem relação com atitude. O movimento angular (velocidade e aceleração angulares) se refere à orientação do objeto e como ela muda. A atitude é a "foto" da orientação em um determinado momento, e o movimento angular é a "virada" ou "filme" dessa atitude mudando.

Em resumo:

* Posição → Velocidade (linear) → Aceleração (linear)

* Atitude → Velocidade angular → Aceleração angular

#### 2.2.1 Euler Attitude

Os ângulos de Euler são uma maneira de descrever a atitude, particularmente a de uma estrutura corporal em relação à estrutura de navegação local correspondente.

**Atitude** é a orientação final do objeto. Por exemplo, a posição de um avião inclinado para a esquerda com o nariz para cima.

Para chegar a essa posição final a partir de uma posição inicial, a matemática de Euler descreve o processo como uma sequência de três rotações simples e sucessivas.

**"rotação" e "inclinação" na física se referem ao mesmo tipo de movimento**

A inclinação é um tipo de rotação. O giroscópio mede a velocidade de rotação, e essa velocidade é o que causa a inclinação.

**REVISÂO DE SENO E COSSENO

Seno e Cosseno no Triângulo Retângulo

A forma mais fácil de entender seno (sen) e cosseno (cos) é em um triângulo retângulo (o triângulo que tem um ângulo de 90 graus).

* Hipotenusa: É o lado mais longo, sempre oposto ao ângulo de 90 graus.

* Cateto Adjacente: O lado do triângulo que está ao lado do ângulo que você está analisando.

* Cateto Oposto: O lado do triângulo que está oposto ao ângulo que você está analisando.


Com isso em mente, as definições são simples:

* Cosseno (cos) de um ângulo é a razão entre o Cateto Adjacente e a Hipotenusa.

        cos(θ)= Cateto Adjacente​/Hipotenusa

* Seno (sen) de um ângulo é a razão entre o Cateto Oposto e a Hipotenusa.

        sen(θ)= Cateto Oposto​/Hipotenusa

**Voltando ao livro**
A primeira rotação, ψβα, é a rotação de guinada(Yaw). Ela é realizada em torno do eixo z comum do quadro β e do primeiro quadro intermediário. Ela transforma as componentes x e y do vetor, mas deixa a componente z inalterada. O vetor resultante é resolvido em torno dos eixos do primeiro quadro intermediário, denotados pelo sobrescrito, ψ:

* A notação ψβα significa "a rotação ψ (psi) do quadro α em relação ao quadro β". Ela define o ângulo de Yaw.

* O eixo de rotação é o eixo Z. Isso faz todo o sentido, pois virar para a esquerda ou para a direita acontece no plano horizontal. O eixo vertical (Z) é o "ponto fixo" em torno do qual essa rotação ocorre.

Quando um objeto gira em torno do eixo Z, duas coisas acontecem com as coordenadas de qualquer vetor:

1. As coordenadas X e Y mudam porque o vetor se move no plano horizontal.

2. A coordenada Z não muda, pois o vetor não se move para cima ou para baixo.

x′=x⋅cos(ψ)+y⋅sin(ψ)

y′=−x⋅sin(ψ)+y⋅cos(ψ)

z′=z

O que essas equações fazem é pegar as coordenadas originais do vetor (x, y, z) e, usando o seno e o cosseno do ângulo de Yaw (ψ), calcular as novas coordenadas (x', y', z') no novo quadro de referência (o "primeiro quadro intermediário").

* A nova coordenada x' é uma mistura das coordenadas x e y originais, ponderada pelo cosseno e pelo seno do ângulo de rotação.

* A nova coordenada y' também é uma mistura, mas com os sinais ajustados para que a rotação seja correta.

* A coordenada z' é simplesmente igual à coordenada z original, confirmando que a altura do vetor não se alterou.

Em seguida, a rotação do pitch, Θβα, é realizada em torno do eixo y comum do primeiro e segundo quadros intermediários. Aqui, as componentes x e z do vetor são transformadas, resultando em um vetor resolvido em torno dos eixos do segundo quadro intermediário, denotado pelo sobrescrito,Θ.

x′=x⋅cos(Θ)- z⋅sin(Θ)

y′= y

z′= x⋅sin(Θ)+ z⋅cos(Θ)

Por fim, a rotação do rolo(Roll), φβα, é realizada em torno do eixo x comum do segundo quadro intermediário e do quadro, transformando as componentes y e z e deixando o vetor resolvido em torno dos eixos do quadro.

x´ = x
y´= y.cos(φ) + z.sin(φ)
z´= - y .sin(φ) + z. cos(φ)

Embora seja mais fácil ilustrar os ângulos de Euler em termos de transformação dos eixos de resolução de um vetor, as rotações de rolamento(Roll), inclinação(Pitch) e guinada(Yaw), φβα, Θβα, e ψβα, descrevem igualmente a orientação do referencial do objeto, α, em relação ao referencial, β.

Relação entre os termos genéricos dos ângulos de Euler (roll, pitch, yaw) e os termos específicos da navegação (bank, elevation, heading).

**Termos Genéricos vs. Termos de Navegação**

A atitude é a orientação do body frame (referencial do objeto) em relação ao local navigation frame (referencial de navegação local, como Norte-Leste-Para Baixo). O texto define como cada uma das três rotações é chamada neste contexto:

* Roll (Rotação em torno do eixo X) é chamado de Bank. Pense no "bank" como a inclinação lateral das asas de um avião ao fazer uma curva. O termo técnico $\phi_{nb}$ representa a rotação de roll do body frame (b) em relação ao navigation frame (n).

* Pitch (Rotação em torno do eixo Y) é chamado de Elevation. A "elevation" é a arfagem do nariz do avião para cima ou para baixo. O termo $\theta_{nb}$ representa a rotação de pitch.

* Yaw (Rotação em torno do eixo Z) é chamado de Heading ou Azimuth. O "heading" é a direção para a qual o objeto está apontando em relação ao Norte. O termo $\psi_{nb}$ representa a rotação de yaw.

A Variação na Terminologia

O texto aponta para uma ambiguidade comum na literatura:

* Alguns autores usam a palavra "atitude" para se referir apenas ao Bank e à Elevation (as inclinações), excluindo o Heading. Eles consideram que o Heading pode ser um parâmetro separado.

* O texto esclarece que, na maioria dos casos, o termo "atitude" é usado para descrever todas as três componentes (bank, elevation e heading) que, juntas, definem completamente a orientação do objeto no espaço.

Tilts (Inclinações)

O trecho também introduz o termo "tilts" (inclinações) para se referir coletivamente ao Bank e à Elevation. Isso é útil porque essas duas rotações descrevem o quanto o objeto está inclinado em relação ao plano horizontal. O Heading, por outro lado, descreve para qual direção no plano horizontal o objeto está virado.

Em resumo, o texto está definindo o vocabulário para as rotações de Euler no contexto da navegação, esclarecendo que os termos Bank, Elevation e Heading são os equivalentes técnicos para Roll, Pitch e Yaw, respectivamente. Ele também ressalta a importância de verificar como cada autor define "atitude", mas adota a convenção mais abrangente de incluir as três rotações.

A rotação de Euler de um quadro de referência para outro pode ser representada por um vetor.

**O Vetor de Rotação de Euler**

Neste contexto, o vetor de rotação de Euler não é o mesmo que um vetor de posição ou velocidade. Ele é um vetor especial que encapsula a orientação, e tem a seguinte forma:
ϵba​=​[ϕθψ]​​

* ϵβα​ representa a atitude (orientação) do quadro β em relação ao quadro α.

* ϕ (phi) é o ângulo de Roll.

* θ (theta) é o ângulo de Pitch.

* ψ (psi) é o ângulo de Yaw.

Este vetor de três componentes é uma forma compacta de armazenar a atitude do objeto. É a representação numérica dos ângulos de Roll, Pitch e Yaw.

Exemplo Prático:

Se um avião está voando em linha reta, sua atitude pode ser representada por um vetor de Euler:

ϵaviao​=​[0° 0° 0°]

Se o avião empina o nariz em 10 graus (Pitch), a atitude dele seria:

ϵaviao​=​[0° 10° 0​°]

Se ele também inclinar as asas em 20 graus (Roll), a atitude se tornaria:

ϵaviao​=​[20° 10° 0°​​]

Então, o "vetor" de rotação de Euler é a maneira mais simples de representar os três ângulos que, juntos, definem a orientação de um objeto.

A ordem em que as três rotações são realizadas é crítica. Se elas forem realizadas em uma ordem diferente (por exemplo, com o rolamento primeiro), a orientação dos eixos no final da transformação geralmente é diferente. Em termos formais, as três rotações de Euler não comutam.

1. Limitação da Rotação de Pitch para Evitar Duplicidade

Esta primeira parte se refere a um problema matemático conhecido como "gimbal lock" (bloqueio do cardan).

* O que causa o problema? Quando a rotação de Pitch (arfagem), que é feita em torno do eixo Y, atinge +90° ou −90°, o eixo em torno do qual a rotação de Roll (eixo X) é feita se alinha perfeitamente com o eixo em torno do qual a rotação de Yaw (eixo Z) é feita.

* A consequência: Quando esses dois eixos se alinham, o sistema perde um "grau de liberdade". Uma rotação pode ser interpretada como uma guinada (yaw) ou uma inclinação (roll), e não há como distinguir. Isso significa que um número infinito de combinações de ângulos de Euler pode representar a mesma orientação, causando ambiguidade e falha nos cálculos de navegação.

* A solução: Para evitar essa falha, a convenção padrão é limitar o ângulo de Pitch ao intervalo de −90° a 90°. Essa limitação impede que os eixos de Roll e Yaw se alinhem, garantindo que cada conjunto de ângulos de Euler corresponda a uma única e exclusiva orientação.

2. A Não-Ortogonalidade dos Eixos de Rotação

Esta segunda parte se refere à natureza sequencial das rotações de Euler.

* O que são eixos ortogonais? Eixos ortogonais são aqueles que formam um ângulo de 90° entre si (como os eixos X, Y e Z de um sistema de coordenadas fixo).

* Por que eles não são ortogonais na prática? As rotações de Euler não são feitas em torno de eixos fixos. Em vez disso, cada rotação é feita em torno de um eixo que já foi rotacionado pela etapa anterior:

    1. A rotação de Yaw é feita em torno do eixo Z original.
    
    2. A rotação de Pitch é feita em torno do eixo Y que já foi rotacionado pela guinada.
    
    3. A rotação de Roll é feita em torno do eixo X que já foi rotacionado tanto pela guinada quanto pela arfagem.

* O resultado: Como o eixo de Roll e o eixo de Yaw são, na verdade, eixos de quadros intermediários que não estão mais alinhados em um ângulo de 90° um com o outro, eles não são ortogonais. O eixo de Pitch, no entanto, é sempre ortogonal aos outros dois eixos em cada etapa da rotação.

Para reverter uma rotação de Euler, a operação original deve ser revertida, começando com o rolamento, ou uma transformação diferente deve ser aplicada. Simplesmente reverter o sinal dos ângulos de Euler não retorna à orientação original. Da mesma forma, rotações sucessivas não podem ser expressas simplesmente pela adição dos ângulos de Euler

#### 2.2.2 Coordinate Transformation Matrix
A matriz de transformação de coordenadas é uma matriz 3 × 3, denotada por Cβα (alguns autores usam R ou T). Quando usada para transformar um vetor de um conjunto de eixos de resolução
para outro, o índice inferior representa o quadro de coordenadas "de" e o índice superior, o quadro "para". As linhas de uma matriz de transformação de coordenadas estão no quadro ‘‘para’’, enquanto as colunas estão no quadro ‘‘de’’.

**Para obter as componentes de um vetor no quadro β, você deve multiplicar o vetor cujas componentes estão no quadro α pela matriz de transformação que vai de α para β**

xδγβ​=Cαβ​ xδγα​

Análise de Cada Componente

x: Este é o vetor. Como discutimos, ele representa uma grandeza física com magnitude e direção, como aceleração, velocidade ou força.

1. xδγα​: Esta parte é o vetor original.

* O sobrescrito α indica que as componentes do vetor estão expressas (resolvidas) no sistema de coordenadas α.

* O subscrito δγ (lê-se "delta gamma") é uma notação mais avançada que especifica os quadros cujo movimento está sendo descrito. Ele significa "o vetor que descreve o movimento do quadro γ em relação ao quadro δ".

2. xδγβ​: Esta é a parte do vetor transformado.

* O sobrescrito β indica que as componentes do vetor agora estão expressas no sistema de coordenadas β.

* O subscrito δγ permanece o mesmo, pois o vetor físico não mudou; apenas a sua representação numérica mudou.

δγ​: Esta notação, como eu disse, significa que o vetor descreve a relação do quadro γ com o quadro δ. Para o nosso exemplo, se γ é o Body Frame e δ é o Navigation Frame, o vetor x descreve a aceleração do drone no Nav Frame.

3. Cαβ​: Esta é a Matriz de Transformação de Coordenadas (ou Matriz de Rotação).

* O sobrescrito β e o subscrito α juntos, Cαβ​, significam "a matriz que transforma um vetor do quadro α para o quadro β".

* Esta matriz é a nossa antiga conhecida, que você viu ser construída com os senos e cossenos dos ângulos de Euler (Roll, Pitch, Yaw).

**O Propósito da Conversão** 

* O sistema de navegação NÃO sabe a atitude do objeto. O giroscópio dá apenas uma estimativa da atitude.

* O sistema de navegação usa a estimativa da atitude para construir a matriz de rotação Cαβ​.

* O sistema usa essa matriz para converter o vetor de gravidade que ele mediu no Body Frame (xα) para o Navigation Frame (xβ).

* A conversão não "dá" a atitude. Em vez disso, a conversão permite que o sistema de navegação verifique se a atitude estimada está correta. Ele faz isso comparando o vetor xβ que ele acabou de calcular com o vetor ideal da gravidade no Nav Frame, que ele sabe que é (0, 0, 9.8).

* Se o vetor x^β calculado for (0.1, 0.2, 9.7), o sistema sabe que há um erro na sua atitude inicial, e ele usa essa diferença para corrigir o cálculo.

O vetor de gravidade se torna o padrão de referência que o sistema usa para se auto-corrigir. Ele não é o resultado final da atitude; ele é a ferramenta que valida e refina a atitude.

O cálculo da atitude com base na fusão de sensores não é um processo de uma única etapa. É um ciclo contínuo de estimação e correção.

Aqui está a lógica que você capturou:

1. Estimação (pelo Giroscópio): O giroscópio fornece a melhor estimativa em tempo real de como o objeto está girando. O sistema integra essa velocidade angular para prever a nova atitude.

2. Verificação e Correção (pelo Acelerômetro): O acelerômetro oferece um ponto de referência absoluto: a direção da gravidade. O sistema usa a atitude que ele estimou para "prever" onde a gravidade deveria estar no quadro do objeto.

3. Ajuste: A diferença entre a "previsão" de gravidade e a "medição real" do acelerômetro é o erro na atitude. O sistema usa essa diferença para fazer um ajuste e corrigir o valor da atitude.

Essa descoberta de erro e a subsequente correção são o que evita a deriva (drift) do giroscópio e mantém o rastreamento da atitude preciso e confiável a longo prazo.

Quando a matriz é usada para representar a atitude, é mais comum usar o índice superior para representar o referencial, , e o índice inferior para representar o referencial do objeto, . Portanto, a matriz representa a rotação do referencial do objeto para o referencial, a convenção oposta à usada para ângulos de Euler.

**A Convenção dos Ângulos de Euler (Tradicional)**

* Notação: A matriz é representada como Cαβ​, significando "transformar do quadro α para o quadro β".

* Interpretação: No contexto dos ângulos de Euler, o quadro α é o referencial do objeto (body frame) e o quadro β é o referencial de navegação (navigation frame).

* O que ela faz: Esta matriz leva um vetor cujas coordenadas estão no referencial do objeto e o converte para o referencial de navegação.

O trecho sugere que essa convenção é mais comum quando se pensa na orientação do objeto (a atitude). A matriz representa a rotação que "leva" o objeto de volta ao seu referencial de navegação.

A Convenção Oposta (A que o trecho descreve)

* Notação: A matriz é representada como Cβα​, o que significa "transformar do quadro β para o quadro α".

* Interpretação: Neste caso, o quadro β é o referencial de navegação e o quadro α é o referencial do objeto.

* O que ela faz: Esta matriz leva um vetor do referencial de navegação (como a gravidade no nosso exemplo) e o converte para o referencial do objeto.


Diferença fundamental entre as duas convenções:

* Convenção dos Ângulos de Euler (Primeira): A matriz é a rotação que leva o referencial do objeto para o referencial de navegação.

* Convenção Oposta (Segunda): A matriz é a rotação que leva o referencial de navegação para o referencial do objeto.

![Texto alternativo para a imagem](C:\Users\marce\OneDrive\Imagens\Capturas de tela\quadro-matriz.png)

Esse trecho descreve uma forma diferente e mais avançada de pensar sobre a matriz de transformação de coordenadas (Cαβ​) e como ela é construída. Em vez de usar os ângulos de Euler (Roll, Pitch, Yaw), ele mostra como a matriz pode ser entendida e até calculada a partir de um vetor.

**O Papel de Cada Elemento da Matriz (Figura da grade)**

A grade mostra o significado físico de cada componente da matriz Cαβ​. Cada célula da matriz representa a projeção de um eixo do quadro de referência original (α) sobre um eixo do novo quadro de referência (β).

Notação xα > xβ: Isso significa "o componente do eixo αx que aponta na direção do eixo βx."

Exemplo: A célula superior esquerda mostra xα > xβ. O valor nessa célula é o cosseno do ângulo entre o eixo X do quadro α e o eixo X do quadro β.

O que a matriz toda representa: A matriz completa é um "mapa" que te diz, para cada eixo do quadro original (α), o quanto ele se projeta sobre os eixos do novo quadro (β). É uma representação compacta de toda a orientação de um quadro em relação ao outro.


**A Matriz Através do Produto de Vetores (Fórmula)**

A fórmula: 

![Texto alternativo para a imagem](C:\Users\marce\OneDrive\Imagens\Capturas de tela\formula1.png)

demonstra que a matriz de rotação pode ser obtida a partir de um único vetor, desde que você conheça suas componentes nos dois quadros de referência.


* xδγβ​: É o vetor (por exemplo, a gravidade) com suas componentes expressas no quadro de referência final (β).

* xδγαT​: É o mesmo vetor, mas com suas componentes expressas no quadro de referência original (α), e transposto (a coluna se torna uma linha).

* O produto no numerador (xδγβ​xδγαT​): Esta operação é chamada de produto externo e resulta em uma matriz 3x3.

* O denominador (∣x∣²): O produto externo é dividido pela magnitude ao quadrado do vetor para normalizar o resultado, garantindo que a matriz tenha as propriedades corretas de rotação.

Em xδγαT​ a transposição do vetor (xαT) é necessária para que a operação matemática de multiplicação de matrizes funcione corretamente e resulte em uma matriz 3x3

A operação xβxαT é conhecida como produto externo ou produto tensorial. É a multiplicação de um vetor-coluna por um vetor-linha, e o resultado é uma matriz.

* Um vetor-coluna tem dimensões m×1.

* Um vetor-linha tem dimensões 1×n.

* O produto de um vetor-coluna (m×1) por um vetor-linha (1×n) resulta em uma matriz de dimensões m×n.

