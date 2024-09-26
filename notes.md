# Community YOutube KIds 

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
- [X] create co-commenter net
- [X] create video-commenter net
- [ ] arrumar notebook de topic modeling:
    - hyperparametros
    - plots dos topics
    - sentiment analysis
- [ ] Reescrever tudo kkkk
- [ ] create repl-commenter net 
    - users who interacted with each other 
- [ ] repensar co-commenter network
- [ ] https://github.com/cardiffnlp/tweetnlp (ver se tem data cleaning)
    - https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment

## COMMENTER NETWORKS (COMUNIDADES)
- [Commenter Behavior Characterization on YouTube Channels](./refs/comment_behaviour_characterization.pdf)
    - introduz o conceito de co-commenter networks
    - For each channel, a co-commenter network is created where edges represent commenters who 
    have commented on the same video. 
    The weight of the edge indicates the number of videos they have co-commented on.
- [Analyzing Disinformation and Crowd Manipulation Tactics on YouTube](./refs/Analyzing_Disinformation_and_Crowd_Manipulation_Tactics_on_YouTube.pdf)
    - generated co- commenter network by connecting two commenters if they commented on the same video 
    - 
