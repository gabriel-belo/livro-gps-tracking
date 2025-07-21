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

## Capítulo 2- Navigation Mathematics
