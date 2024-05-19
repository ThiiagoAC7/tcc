# Real time classification of fake news considering news content and social context with user preferences (?)
> Thiago Amado Costa 

- Ideia : real-time  classification of news articles by utilizing these content and
context-based features for the real-world dataset (Graph-based dataset).
Real time classification of news articles considering news content and social context.
    - [UPFD](#metodology), mudando para grafos de propagacao menores
        - para ser viavel 
        - identificacao da fake news in real time (early detection)
    -  Propagation graphs:
        1. Hop-based news cascade (nomal, do jeito q ta no artigo)
            - root sendo a noticia (ou o primeiro usuario a compartilhar a noticia),
            - nodes sendo os usuarios que retweetaram etc.
            - representa o alcance da noticia, profundidade
        2. Time-based news cascade:
            - root e nodes igual 
            - representa o tempo de vida da noticia
        3. Propagation Graph where
            - Root is the news
            - First level are "Root Tweets" 
                - tweets that directly reference the URL
            - other nodes are retweets
        4. Spatial–Temporal Similarity Graph (Detection and analysis of fake news user communities): 
            -It generates the graph that connects the users who participate
            in the same news campaigns during the first T time period since the beginning of the campaigns.

## TODO:

- [~] read
    - lido [User Preference-aware Fake news detection](./refs/importantes/2104.12259v1.pdf)
    - lido [FakeNewsNet: A Data Repository with News Content, Social Context and Spatiotemporal Information for Studying Fake News on Social Media](./refs/importantes/fake_news_net.pdf)
    - lido [Fake News Tracker](./refs/importantes/FakeNewsTracker_a_tool_for_fake_news_collection_de.pdf)
    - lido [Graph Neural Networks with Continual Learning for Fake News Detection from Social Media](./refs/importantes/Graph Neural Networks with Continual Learning for Fake News.pdf)
    - lido [A survey of fake news](./refs/importantes/1812.00315v2.pdf)
    - lido [Detection and analysis of fake news user communities](./refs/communities/Detection_and_Analysis_of_Fake_News_Users_Communities_in_Social_Media.pdf)
    - [Early Detection of Fake News on Social Media Through Propagation Path Classiﬁcation with Recurrent and Convolutional Networks](./refs/3504035.3504079.pdf)
    - [Geometric Deep Learning - GCNFN](./refs/geometric_deep_learning.pdf)
    - [Leveraging Multi-Source Weak Social Supervision for Early Detection of Fake News.](./refs/2004.01732v1.pdf)
    - [Fake News Early Detection: A Theory-driven Model](./refs/3377478.pdf)
- [~] definir o que vou retirar de cada artigo em cada ./refs/importantes/
- [~] ENTENDER GNN - GRAPH NEURAL NETWORKS  <--
- [~] ESTUDAR EARLY DETECTION DE FAKE NEWS  <-- 
- [ ] Mudar Related Work, Introduction
- [X] organizacao metodologia -> fazer diagrama:
- [x] review on [echo chambers (for graph based community identification)](./refs/echo_chambers.md)
- [x] Pensar em um caminho a partir de um artigo de interesse:
    - Replicar a metodologia com outro contexto/dataset
    - Estender as análises de um artigo de interesse, por exemplo, agregando outros datasets como o NOW Corpus 
    - Analise de Echo Chambers X Analise de Modelo?
        - mais facil (?) analise e comparacao de modelo
- [ ] escolher dataset
    - PROBLEMAS :
    - twitter mudou de politicas para desenvolvedores, codigo da FakeNewsNet pode ter que mudar
    - USAR alternativas da API do twitter


## Tools
- [whisper](https://github.com/Vaibhavs10/insanely-fast-whisper) 
    - transcribe audio files
- [speech_recognition](https://github.com/Uberi/speech_recognition)
    - Library for performing speech recognition, with support for several engines and APIs, online and offline 
- [NOW corpus](https://www.corpusdata.org/now_corpus.asp)
    - NOW corpus contains data from 32,217,384 texts from online magazines and newspapers in 20 different English-speaking countries from 2010 to the current time
- [NOW corpus portugues](https://www.corpusdoportugues.org/now/)
    - The Corpus do Português NOW corpus (News on the Web) contains about 1.1 billion words of data from web-based newspapers and magazines in four Portuguese-speaking countries from 2012-2019. 
- [Netwokrx](https://networkx.org/)
    - creation, manipulation, and study of the structure, dynamics, and community of networks.  
- Dataset :
    - [FakeNewsNet](https://github.com/KaiDMML/FakeNewsNet)
        - First, the rich set of features in the datasets provides an op-
        portunity to experiment with different approaches for fake
        new detection, understand the diffusion of fake news in so-
        cial network and intervene in it. Second, the temporal in-
        formation enables the study of early fake news detection by
        generating synthetic user engagements from historical tem-
        poral user engagement patterns in the dataset. 
        Third, we can investigate the fake news diffusion pro-
        cess by identifying provenances, persuaders, and developing
        better fake news intervention strategies

## Related Work Structure

- Classify existing work into three categories: 
    -content-based approaches,
        - knowledge based
        - style based
            - the purpose of fake news is to mislead the public, they often exhibit unique writing styles that are rarely seen in real news.
    -context-based approaches 
        - For example, Jin et al. build a stance network where the weight of an edge represents how much each pair of
    posts support or deny each other. Then fake news detection is based on estimating the credibility of all the posts related to the news
    item, which can be formalised as a graph optimisation problem
            - Zhiwei Jin, Juan Cao, Yongdong Zhang, and Jiebo Luo. 2016. News Verification by Exploiting Conflicting Social Viewpoints in Microblogs. In Proceedings of the 30th AAAI (AAAIâĂŹ16). Phoenix, Arizona, 2972–2978.
    - mixed approaches, 
    - the first two of which, as suggested by their names, mainly rely on news content and social context to extract features for detection, respectively.
- Importants
    - UPFD:
        - The research paper's approach emphasizes the importance of considering user preferences in fake news detection, as users are more likely to spread fake news that aligns with their existing beliefs or preferences.

## Metodology

- fake news propagation graph ([User Preference-aware Fake news detection](./refs/importantes/2104.12259v1.pdf))  
    - based on the Confirmation Bias (users tend to believe in news that confirm their opinions, and not believe in oposite opinions)
    - grafo de propagacao da fake news 
        - diferentes tipos de representacao de grafo
    - fazer isso para outra rede social alem do twitter (Facebook) (?)
        - Utilizar a metodologia do artigo para construir um dataset do Facebook e verificar se funciona tambem (?)
    - (UPFD) Twitter APIs only show that B, C, D, and E are retweets of A, but E is actually a retweet of C. To solve
        this problem, within each cascade we first sort the tweets by their timestamps, and then search for the source of a retweet from all
        the tweets that are published earlier. Specifically, there is an edge from node i to node j 3 if:
            - The user of node i mentions the user of node j in the tweet, e.g., user i retweets a news item and also recommends it to user j via mentioning; 
            - Tweet i is public and tweet j is posted within a certain period of time after tweet i. We have tested different time limits from one hour to ten hours.

- adicionar comentarios ao dataset (?)
    - Endogenous information (textos)
    - BERT is better than word2vec for encoding textual features which has been verified on other NLP tasks. 
    Note that the BERT performance could be further improved via fine-tuning, and we leave it as future work.

- se for comparar 2 ou mais modelos no UPFD
    - baseline [FakeNewsNet - Experimentos](./refs/importantes/fake_news_net.pdf)

- real-time text-based classification:
    - testar modelo(s) com nova noticia
    - noticia passa pelo pipeline (grafo de propagacao, news/context)
    - propagation path after 5 min (example) 

- train on 2 datasets separately 

- The sturcture of the propagation graph is also slightly changed, to be a Time-based news cascade that
allows a measure of real-time heat (the number of users posting/reposting the news at a given time t), 
as explained by \cite{Zhou_2020}.

### Early Detection
    - we train GNNs on the clipped dataset that contains for each news item (1) the first 100, 200, 500, 1000 tweets (green
    bars in Figs. 2 and 3); and (2) the first 100 tweets or tweets from the first one, three, five or seven hours,
        - [Graph Neural Networks with Continual Learning for Fake News Detection from Social Media](./refs/importantes/Graph Neural Networks with Continual Learning for Fake News.pdf)
    - USAR ISSO COM FRAMEWORK UPFD proposto pra ver se eh bao msm
    - Continual Learning
        - Catastrophic forgetting : when a deep neural network is trained to learn a sequence of tasks, it degrades its performance on
        the former tasks after it learns new tasks, as the new tasks override the weights.
    - The propagation graph on the early stages of a fake news probably has less nodes
        - a time T must be set

## Future Work
possible expansions of this work

1. Utilize the [FakeNewsTracker](./refs/importantes/FakeNewsTracker_a_tool_for_fake_news_collection_de.pdf)
and the [FakeNewsNet](./refs/importantes/fake_news_net.pdf) methodology to create another dataset for :  
    1. News in another language (such as portuguese) 
    2. News in other social media (instagram/facebook)

That enables further studies, to see if the same Fake News spreads differently in different countries, for example

## References

- Fake News and Real News spread differently online 
    - Soroush Vosoughi, Deb Roy, and Sinan Aral. 2018. The spread of true and false news online. Science 359, 6380 (2018), 1146–1151.

- It is critical to detect fake news at an early stage before it becomes widespread,
  since the wider fake news spreads, the more likely people would trust it 
    - Lawrence E. Boehm. 1994. The Validity Effect: A Search for Mediating Variables. Personality and Social Psychology Bulletin 20, 3 (1994), 285–293.

- it is difficult to correct people’s perception towards an issue, even if the previous impression is inaccurate .
    - Jonas De keersmaecker and Arne Roets. 2017. âĂŸFake newsâĂŹ: Incorrect, but hard to correct. The role of cognitive ability on the impact of false information on social impressions. Intelligence 65 (2017), 107 – 110.

