# Identifying (deep) fake news communities on multiple social networks

- Ideia : real-time text-based classification of news articles by utilizing these content and
context-based features for the real-world dataset (Graph-based dataset)
    - pegar uma nova noticia e fazer o processo do dataset (input)
- Ideia 2 (!!):
    - [UPFD](#metodology) com 2 propagation graphs:
        1. Hop-based news cascade (nomal, do jeito q ta no artigo)
            - root sendo a noticia (ou o primeiro usuario a compartilhar a noticia),
            - nodes sendo os usuarios que retweetaram etc.
            - representa o alcance da noticia, profundidade
        2. Time-based news cascade:
            - root e nodes igual 
            - representa o tempo de vida da noticia

> Thiago Amado Costa

## TODO:

- [] read
    - lido [User Preference-aware Fake news detection](./refs/importantes/2104.12259v1.pdf)
    - lido [FakeNewsNet: A Data Repository with News Content, Social Context and Spatiotemporal Information for Studying Fake News on Social Media](./refs/fake_news_net.pdf)
    - [Fake News Tracker](./refs/FakeNewsTracker_a_tool_for_fake_news_collection_de.pdf)
    - [Graph Neural Networks with Continual Learning for Fake News Detection from Social Media](./refs/Graph Neural Networks with Continual Learning for Fake News.pdf)
    - [A survey of fake news](./refs/1812.00315v2.pdf)
    - ...

- [] GNN - graph neural networks 
    - entender

- [~] review on [echo chambers (for graph based community identification)](./refs/notes/echo_chambers.md)
- [] Pensar em um caminho a partir de um artigo de interesse:
    - Replicar a metodologia com outro contexto/dataset
    - Estender as análises de um artigo de interesse, por exemplo, agregando outros datasets como o NOW Corpus 
    - Analise de Echo Chambers X Analise de Modelo?
        - mais facil (?) analise e comparacao de modelo

- [~] organizacao metodologia -> fazer diagrama:
    1. Community Detection (echo chambers - definicao de cada echo chamber)
    2. Fake News Detection (em cada echo-chamber)
    3. Analise disso 

- [X] escolher dataset


## Tools
- [whisper](https://github.com/Vaibhavs10/insanely-fast-whisper) 
    - transcribe audio files
- [speech_recognition](https://github.com/Uberi/speech_recognition)
    - Library for performing speech recognition, with support for several engines and APIs, online and offline 
- [NOW corpus](https://www.corpusdata.org/now_corpus.asp)
    - NOW corpus contains data from 32,217,384 texts from online magazines and newspapers in 20 different English-speaking countries from 2010 to the current time
- [NOW corpus portugues](https://www.corpusdoportugues.org/now/)
    - The Corpus do Português NOW corpus (News on the Web) contains about 1.1 billion words of data from web-based newspapers and magazines in four Portuguese-speaking countries from 2012-2019. 
- Datasets :
    - buzzfeed
    - polifact
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

## Concepts

- Infodemic
- Echo Chambers

## Metodology

- fake news propagation graph ([User Preference-aware Fake news detection](./refs/2104.12259v1.pdf))  
    - based on the Confirmation Bias (users tend to believe in news that confirm their opinions, and not believe in oposite opinions)
    - grafo de propagacao da fake news 
    - fazer isso para outra rede social alem do twitter (Facebook) (?)
        - Utilizar a metodologia do artigo para construir um dataset do Facebook e verificar se funciona tambem (?)

- adicionar comentarios ao dataset (?)
    - Endogenous information (textos)
    - BERT is better than word2vec for encoding textual features which has been verified on other NLP tasks. 
    Note that the BERT performance could be further improved via fine-tuning, and we leave it as future work.

- se for comparar 2 ou mais modelos no UPFD
    - baseline [FakeNewsNet - Experimentos](./refs/importantes/fake_news_net.pdf)

- real-time text-based classification:
    - testar modelo(s) com nova noticia
    - noticia passa pelo pipeline (grafo de propagacao, news/context)


## References

### Fake News / Fact Checking

- [A Survey of Fake News: Fundamental Theories, Detection Methods, and Opportunities](./refs/notes/a_survey_of_fake_news.md)

### Community / Context

- [Near linear time algorithm to detect community structures in large-scale networks.pdf](./refs/notes/community_structures.md)
- [A social community detection algorithm based on parallel grey label propagation]()
- [Beyond News Contents: The Role of Social Context for Fake News Detection]()
- [Graph-based Modeling of Online Communities for Fake News Detection]()

#### Echo Chambers
- [DeepFakE: improving fake news detection using tensor decomposition‑based deep neural network](./refs/notes/echo_chambers.md)


