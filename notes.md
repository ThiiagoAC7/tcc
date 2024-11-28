# Community YOutube KIds 

## ARRUMAR:

Antes de partir as conclusões e trabalhos futuros, precisa de
um fechamento dos resultados. 
Esse fechamento é feito a partir da interpretação do que se pode aprender com os resultados.
É possível compará-los? 
Tem algum tipo de padrão ou é tudo aleatório? 

Você conseguiria caracterizar melhor cada comunidade, dando um nome significativo para cada uma

Eu acho que o caminho seria comparar as comunidades dos diferentes YouTubers tentando comparar 
os clusters, por exemplo, colocando suas caracterítcas em tabelas.


## Methodology

- [Topic Modeling to identify Abusive comments](./refs/Utilizing_Topic_Modelling_To_Identify_Abusive_Comments_On_YouTube.pdf)
    ![meth](./refs/meth.png) 
    - We have used LDA (latent Dirichlet allocation) to identify dominant topics in a particular 
    uploader’s comment section. 
    - We have also used the TextBlob library of python for determining the polarity and 
    subjectivity of comments for each uploader.

- Analise exploratoria de dados
- Topic Modeling
- Sentiment Analysis 

## TODO:
- [ ] Reescrever tudo;
    - [ ] justificar que existem muitas pesquisas com analise de comunidade, mas nao tem muito
    em analise de comunidade em videos infantis.
- [ ] repensar co-commenter network
    - https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment

## COMMENTER NETWORKS (COMUNIDADES)
- [Commenter Behavior Characterization on YouTube Channels](./refs/comment_behaviour_characterization.pdf)
    - For each channel, a co-commenter network is created where edges represent commenters who 
    have commented on the same video. 
    The weight of the edge indicates the number of videos they have co-commented on.
- [Analyzing Disinformation and Crowd Manipulation Tactics on YouTube](./refs/Analyzing_Disinformation_and_Crowd_Manipulation_Tactics_on_YouTube.pdf)
    - generated co- commenter network by connecting two commenters if they commented on the same video 
    - video-commenter network
- [Towards Characterizing Coordinated Inauthentic Behaviors on YouTube](./refs/coordinated_inauthentic_behaviour.pdf) 
    - To declutter the network and focus on the suspicious network clusters, we filtered out
    commenter (node) pairs (low-weight edges) if they co-commented on less than 10 videos.
    This threshold number is adjustable in practice. Nevertheless, because of our initial experiments, 
    we fixed the current threshold for co-commenter pairs to 10 to cover as many channels as possible 
    and include edges that signal frequent interactivity, while eliminating the random chance 
    of co-commenter pairings.

### METRICS:
- Community Detection Algorithms:
    - k-cliques (nao rodou)
    - label propagation (testar)
    - louvain_communities (rodou)
    - greedy modularity (testar)

## References:

### COMMUNITY DETECTION:
- LOUVAIN ALGORITHM:
    - Louvain Community Detection Algorithm is a simple method to extract the community structure 
    of a network. This is a heuristic method based on modularity optimization.
    - usar [artigo](./refs/communities/A three-stage algorithm on community detection in social networks.pdf)
    para justificar o uso do Louvain.
        - comunidades distintas.


- MODULARITY:
    - see [Finding community structure in very large networks](./refs/graph_metrics/Finding community structure in very large networks.pdf)
    - Nonzero values represent deviations from randomness, and in practice it is found
    that a value above about 0.3 is a good indicator of significant community structure in a network.

### BRazil:
- Crianca e Consumo: https://criancaeconsumo.org.br/nossa-atuacao/atuacao-juridica/acoes-juridicas/mattel-do-brasil-ltda-voce-youtuber-escola-monster-high-fevereiro2017/
- https://cgi.br/noticia/releases/tic-kids-online-brasil-2023-criancas-estao-se-conectando-a-internet-mais-cedo-no-pais/
- https://cetic.br/pt/pesquisa/kids-online/
- https://alana.org.br/material/o-trabalho-infantil-artistico-no-ambiente-digital/ 

### Children's Safety on Youtube: A systematic review

- However, some users exploit this possibility to misuse social media platforms by posting abusive
content and deliberately affronting others. Duggan (2017) reported that a large number of
users on social media have experienced abusive behavior, or have observed cases of
harassment directed to other fellows.
    - Duggan M. 2017. Online harassment 2017. Available at 
        https://www.pewresearch.org/internet/ 2017/07/11/online-harassment-2017/.
- Research has shown that these events not only lead to mental stress and anxiety in users but, 
in some cases, individuals end up shutting down their social media accounts and, in extreme cases, 
even causes individuals to take their own lives
    - Hinduja S, Patchin JW. 2010. Bullying, cyberbullying, and suicide. Archives of Suicide Research
    14(3):206–221 DOI 10.1080/13811118.2010.494133.
    - Ashraf N, Mustafa R, Sidorov G, Gelbukh A. 2020. Individual vs. group violent threats
    classiﬁcation in online discussions. In: Companion Proceedings of the Web Conference 2020,
    WWW ’20. New York: Association for Computing Machinery, 629–633.
    - Mustafa RU, Ashraf N, Ahmed FS, Ferzund J, Shahzad B, Gelbukh A. 2020. A multiclass
    depression detection in social media based on sentiment analysis. In: Latiﬁ S, ed. 17th
    International Conference on Information Technology-New Generations (ITNG 2020). Cham:
    Springer International Publishing, 659–662.
- YouTube is leading the market for kid-oriented videos.
    - Kavya Agarwal Should Your Young Child Watch YouTube? Pros and Cons. Available online: https://www.blackboardradio.com/
post/should-your-young-child-watch-youtube-pros-and-cons
    - pros: Help in upskilling, fostering creativity, academic resource
    - cons: exposure to innapropriate content, contact with wrong information, creating false projetion

### Towards Characterizing Coordinated Inauthentic Behaviors on YouTube

- Pacheco et al. [25] introduced an unsupervised and network structure-based methodology to 
detect coordinated communities on social media.
    - Pacheco, D., Hui, P. M., Torres-Lugo, C., Truong, B. T., Flammini, A., & Menczer, F. (2021,
    May). Uncovering Coordinated Networks on Social Media: Methods and Case Studies. In
    Proceedings of the International AAAI Conference on Web and Social Media (Vol. 15, pp. 455-
    466).
