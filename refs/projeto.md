# Classificação em tempo real de Fake News considerando o conteúdo textual e conteúdo social.

> Thiago Amado Costa

## 1. Resumo

O fenômeno das Fake News se tornou um desafio significativo na era da mídia social, 
representando sérias ameaças à credibilidade das informações compartilhadas on-line. 
Além disso, indivíduos e grupos específicos podem se tornar alvos dessas ações maliciosas, 
criando comunidades que acreditam e compartilham notícias das mesmas fontes maliciosas. 
Atualmente, pesquisas demonstram a importância da detecção de notícias falsas, principalmente
em seus estágios iniciais de propagação, utilizando diferentes abordagens. 
Este estudo aborda esse desafio, ao utilizar um método que integra duas abordagens distintas
que consideram tanto o conteúdo textual da notícia como o conteúdo social, adaptando-as 
para a detecção precoce de notícias falsas.

## 2. Introdução

O fenômeno das Fake News é, atualmente, uma dos maiores desafios para a sociedade moderna,
ameaçando a credibilidade das informações compartilhadas online. Segundo [Lazer et al. (2018)],
Fake News é definida como informação incorreta ou enganosa fabricada para imitar a estrutura das mídias de notícias,
mas sem o processo de garantir a precisão e credibilidade.

Esse fenômeno representa sérias ameaças às mídias sociais atuais, pois se 
espalha mais rapidamente e de forma mais ampla do que as informações confiáveis, 
conforme [Vosoughi et al. (2018)]. 
Além disso, segundo [Zhou e Zafarani (2020)], 
quanto mais uma notícia falsa se espalha, maior a probabilidade de pessoas 
confiarem e acreditarem nelas, o que se torna um sério problema considerando também que 
notícias falsas são criadas e publicadas de forma mais fácil e rápida em mídias sociais 
do que em mídias tradicionais.

A existência do efeito das chamadas *echo chambers* (câmaras de eco) nas redes sociais também é um 
agravante ao problema. Esse conceito pode ser definido, segundo [Cinelli et al. 2021], como
grupos de indivíduos que se envolvem em torno de opiniões, crenças e inclinações 
políticas parecidas, possuindo tendências e atitudes similares. Ainda, a existência dessas 
câmeras de eco podem reforçar e levar esses indivíduos a desenvolverem ideais cada vez mais
extremos. 
Considerando esse efeito, informações tendenciosas são reforçadas e ampliadas, causando efeitos 
diferentes de acordo com o grupo atingido ([Zhou e Zafarani (2020)]).

Isso reforça a necessidade de mais estudos e desenvolvimento de metodologias de detecção de Fake News,
principalmente em seus estágios iniciais. Nesse contexto, o *User Preference-aware FakeNews Detection Framework* 
(Detecção de Notícias Falsas Sensível às Preferências do Usuário - UPFD), proposto por [Dou et al. 2021],
além de utilizar informações textuais das notícias para a detecção de fake news, 
utiliza informações sociais dos usuários que as propagaram, o que segundo os autores 
desempenha um papel fundamental nessa detecção, e o modelo proposto atinge performances consideráveis.
Uma explicação mais detalhada do framework pode ser lida na Metodologia.

Dessa forma, o objetivo desse estudo é adaptar o framework UPFD no contexto de detecção precoce de notícias
falsas, de modo a confirmar a importância dos contextos sociais nessa detecção.

## 3. Conteúdo

Atualmente existem diferentes perspectivas para a detecção automática de notícias falsas, e em sua maioria
utilizam técnicas de Aprendizado de Máquina, Processamento de Linguagem Natural, Teoria dos Grafos, entre outros.

A perspectiva baseada em conteúdo, por exemplo, considera somente o conteúdo textual das notícias, como
o título, descrição, corpo, etc. A perspectiva baseada em contexto explora o contexto da notícia e como 
ela se espalha, baseando em efeitos como as câmaras de eco e utilizando métodos para mapear sua propagação. 
Existem também perspectivas que combinam a análise textual e contextual para a identificação das notícias.

Dentre as principais contribuições da àrea, é possível destacar 
[Ruchansky et al. (2017)], que combina características de texto, resposta e fonte 
de artigos de notícias para abordar a detecção de notícias falsas. Diferentemente das soluções 
existentes que se concentram em aspectos individuais, o modelo CSI integra esses três recursos 
principais usando redes neurais profundas para selecionar automaticamente informações importantes 
e capturar deformações temporais. redes neurais profundas para selecionar automaticamente informações importantes e capturar
pendências temporais no envolvimento do usuário. 
Ao fornecer insights sobre artigos e usuários, o CSI oferece uma compreensão 
mais abrangente da propagação de notícias falsas. Os resultados experimentais em conjuntos 
de dados do mundo real demonstram que o modelo CSI atinge maior precisão de classificação em comparação 
com os métodos anteriores, além de exigir menos parâmetros e esforços de treinamento. 
Isso destaca a eficácia do modelo CSI na detecção precisa de 
notícias falsas e na abordagem dos desafios associados à detecção automatizada de notícias falsas. 

Destaca-se também o estudo de [Kaliyar et al. 2021], que apresenta um novo modelo chamado DeepFakE 
para melhorar a detecção de notícias falsas detecção de notícias falsas combinando 
conteúdo de notícias e contexto social. 
A abordagem combina conteúdo de notícias e recursos baseados em contexto social em um tensor, 
resultando em um de decisão de ordem superior e obtendo resultados de última geração 
para a detecção de notícias falsas. O artigo mostra a importância de examinar o 
contexto social para melhorar a detecção de notícias falsas. 
Ele enfatiza a função do envolvimento social do usuário e das câmaras de eco na 
disseminação de notícias falsas. 
As câmaras de eco, que são grupos de indivíduos que pensam da mesma forma, 
desempenham um papel fundamental na disseminação de notícias falsas, 
pois tendem a compartilhar histórias que se alinham com suas crenças. 
O artigo sugere que utilizar *echo chambers* para obter informações relacionadas ao usuário
e à comunidade a partir de notícias pode aprimorar a detecção de notícias falsas.

Avanços recentes na detecção de notícias falsas nas redes sociais têm cada vez mais 
aproveitado Redes Neurais em Grafos (GNNs) para identificar padrões na propagação de informações, 
independentemente do conteúdo textual. 
Essa abordagem atende à necessidade de discernir entre notícias reais e falsas com base na forma como elas se espalham pelas redes. 
[Han et al. (2020)] propõe um método de detecção baseado na propagação usando GNNs, 
que explora os comportamentos distintos de disseminação de notícias falsas versus reais online. 
Além disso, para enfrentar o desafio de se adaptar a novos e inéditos dados, 
o estudo introduz um método de aprendizado contínuo que mantém um desempenho 
equilibrado entre conjuntos de dados existentes e novos. 
Esse estudo mostra também que a exploração do grafo de propagação das notícias
pode ser utulizada na identificação de notícias falsas, ao mostrar que o mesmo
método em grafos menores também obtém performances consideráveis.

Em outro estudo que foca em detecção precoce de notícias falsas, 
[Zhou et al. 2020] apresenta um modelo orientado por teoria, com foco na análise do conteúdo das notícias 
em vez de sua propagação nas plataformas de mídia social. 
Ao integrar percepções de teorias estabelecidas em psicologia social, 
a pesquisa explora vários níveis de conteúdo de notícias, melhorando assim a interpretabilidade da 
engenharia de recursos de notícias falsas. 
Aproveitando as técnicas de aprendizado de máquina supervisionado, 
o modelo demonstra um desempenho superior em comparação com os métodos existentes, 
demonstrando sua capacidade de obter detecção precoce mesmo quando 
confrontado com informações limitadas sobre o conteúdo.

Dessa forma, considerando os estudos anteriores,
o objetivo desse estudo é adaptar o framework UPFD no contexto de detecção precoce de notícias
falsas, de modo a confirmar a importância dos contextos sociais nessa detecção.
Esse framework combina um método de detecção baseado em grafos com um método baseado em análise do 
conteúdo textual, e será explicado na proxima seção.

## 4. Metodologia

Este estudo utiliza uma combinação de conteúdo textual de noticias e contexto social para detectar 
notícias falsas em seus estágios iniciais, utilizando o repositório de dados *FakeNewsNet* proposto por [Shu, 2019], 
que atualmente contém dois conjuntos de dados diferentes com conteúdo textual específico, 
contexto social e informações espaço-temporais, e uma versão do framework *User Preference-aware FakeNews Detection*
(UPFD) proposto por [Dou, 2021].

### 4.1 Conjunto de dados FakeNewsNet

O conjunto de dados FakeNewsNet é um recurso abrangente projetado para auxiliar na detecção e estudo de notícias falsas. 
Ele oferece diversas características essenciais para análise, incluindo o conteúdo textual das notícias, 
contexto social e informações espaço-temporais.

O FakeNewsNet inclui conjuntos de dados de duas fontes diferentes, Polifact e Gossipcop. 
Uma das vantagens significativas do FakeNewsNet são os dados multidimensionais, que considera o tanto o conteúdo textual 
das notícias como contexto social e iformações espaço-temporais, o que é instrumental para estudar a detecção precoce 
de notícias falsas, sua evolução e possíveis estratégias para minimizar seus danos.

O FakeNewsNet pode ser usado para muitas aplicações de pesquisa diferentes, 
como o estudo e a classificação de notícias falsas em seus estágios iniciais, 
usando o contexto social e as informações espaço-temporais. 
Outra possível aplicação é a identificação de atores maliciosos que desempenham um 
papel poderoso na disseminação de notícias falsas. 
O FakeNewsNet também pode ser expandido, adicionando suporte em diferentes idiomas e diferentes plataformas de mídia social, 
ao reproduzir sua metodoligia, proposta por [Shu, 2019].

### 4.2 Framework UPFD

O framework *User Preference-aware FakeNews Detection* (Detecção de Notícias Falsas Sensível às Preferências do Usuário - UPFD)
extrai o conteúdo textual das notícias e o contexto social dos conjuntos de dados para construir dois Codificadores.

Primeiro, o Codificador Endógeno (ou Codificador Textual das Notícias) 
utiliza técnicas de representação de texto pré-treinadas para gerar o
*Embedding* da informação textual das notícias e dos posts históricos dos usuários que interagiram com as notícias.

O Codificador Exógeno (ou Codificador de Engajamento do Usuário)
constrói um grafo de propagação de notícias onde o nó raiz é a notícia e 
os outros nós representam os usuários que repostaram a notícia. 
Em seguida, usa uma GNN (*Graph Neural Network* - Redes Neurais em Grafos) para fundir as características 
dos usuários com este caminho de propagação da notícia, 
adicionando o *embedding* textual das notícias e o *embedding* das preferências 
dos usuários como características dos nós, para aprender os *embeddings* dos nós.
Aplicando uma função de leitura que realiza a média dos *embeddings* de todos os nós,
o *embedding* do Grafo de Propagação de Notícias é obtido.

Finalmente, é feita uma concatenação entre o 
Embedding Textual da Notícia e o Embedding de Engajamento do Usuário 
para criar o Embedding Final da Notícia, que é alimentado em um Perceptron Multicamadas (MLP) com duas saídas,
representando as probabilidades de notícias reais e falsas. 
O treinamento do modelo utiliza Binary Cross-entropy como função de perda e é atualizado 
com a função de otimização Stochastic Gradient Descent (SGD).

Este framework é ilustrado na Figura 1:

![UPFD Framework](./upfd_framework_page-0001.jpg) 
*Figura 1: Detecção de Notícias Falsas Sensível às Preferências do Usuário - UPFD*

### 4.3 Detecção Precoce de notícias falsas utilizando UPFD

A detecção precoce de notícias falsas é crucial porque, à medida que a disseminação 
de notícias falsas aumenta, torna-se cada vez mais desafiador mitigar seus efeitos. 
Também é importante considerar que notícias falsas se espalham mais amplamente e mais 
rapidamente do que notícias reais, conforme mostrado por [Vosoughi, 2018].

O framework original de Detecção de Notícias Falsas Sensível às Preferências do Usuário (UPFD)
é usado considerando todo o grafo de propagação das notícias. 
Para usá-lo na detecção precoce, o grafo de propagação é cortado para considerar apenas os primeiros 100 
reposts de uma determinada notícia, e apenas 20 posts históricos de um determinado usuário 
que repostou, em vez dos 200 originais. 
Comentários dos usuários sobre o post original da notícia também são considerados. 
Um limite de tempo também é definido, para considerar apenas a primeira hora de disseminação.

O objetivo é determinar se as preferências dos usuários e o contexto social podem desempenhar 
um papel significativo na identificação de notícias falsas em seus estágios iniciais, 
quando o grafo de propagação é menor e menos usuários interagiram com a notícia.

## 5. Referências Bibliográficas:


1. [Lazer, D. M., Baum, M. A., Benkler, Y., Berinsky, A. J., Greenhill, K. M., Menczer, F., Metzger, M. J., Nyhan, B., Pennycook, G., Rothschild, D., et al. (2018). 
The science of fake news. Science, 359(6380):1094–1096.](https://www.science.org/doi/10.1126/science.aao2998)

2. [Dou, Y., Shu, K., Xia, C., Yu, P. S., and Sun, L. (2021). User preference-aware fake news detection.](https://arxiv.org/abs/2104.12259)

3. [Vosoughi, S., Roy, D., and Aral, S. (2018). The spread of true and false news online. Science, 359(6380):1146–1151.](https://www.science.org/doi/10.1126/science.aap9559)

4. [Shu, K., Mahudeswaran, D., Wang, S., Lee, D., and Liu, H. (2019). Fakenewsnet: 
A data repository with news content, social context and spatialtemporal information for fake news detection](https://arxiv.org/abs/1809.01286)

5. [Zhou, X. and Zafarani, R. (2020). A survey of fake news: Fundamental theories, detection, methods, and opportunities. ACM Computing Surveys, 53(5):1–40.]()

6. [Ruchansky, N., Seo, S., and Liu, Y. (2017). Csi: A hybrid deep model for fake news detection. In Proceedings of the 2017 ACM on Conference on Information and Knowledge Management, CIKM ’17. ACM.]()
