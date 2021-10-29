
# Projeto sendo desenvolvido com ChatterBot por um grupo de estagiarios para Mogi2Go 

ChatterBot é um mecanismo de diálogo conversacional baseado em aprendizado de máquina construído em
Python, que torna possível gerar respostas com base em coleções de
conversas conhecidas. O design independente de linguagem do ChatterBot permite
ser treinado para falar qualquer idioma.


## Como funciona

Uma instância não treinada do ChatterBot começa sem nenhum conhecimento de como se comunicar. Cada vez que um usuário insere uma declaração, a biblioteca salva o texto que ele inseriu e o texto ao qual a declaração foi respondida. À medida que o ChatterBot recebe mais entradas, o número de respostas que ele pode responder e a precisão de cada resposta em relação à instrução de entrada aumentam. O programa seleciona a resposta correspondente mais próxima procurando a declaração conhecida mais próxima que corresponda à entrada, ele então retorna a resposta mais provável para aquela declaração com base na frequência com que cada resposta é emitida pelas pessoas com as quais o bot se comunica.

## Instalação

Este pacote pode ser instalado de [PyPi] (https://pypi.python.org/pypi/ChatterBot) executando:

`` `
pip instalar chatterbot
`` `


# Dados de treinamento

O ChatterBot vem com um módulo de utilitário de dados que pode ser usado para treinar bots de bate-papo.
No momento, existem dados de treinamento para mais de uma dúzia de idiomas neste módulo.
Contribuições de dados de treinamento adicionais ou dados de treinamento
em outras línguas seria muito apreciado. Dê uma olhada nos arquivos de dados
no [chatterbot-corpus] (https://github.com/gunthercox/chatterbot-corpus)
pacote se você estiver interessado em contribuir.

`` `
from chatterbot.trainers import ChatterBotCorpusTrainer

# Crie um novo treinador para o chatbot
trainer = ChatterBotCorpusTrainer (chatbot)

# Treinar com base no corpus inglês
trainer.train ("chatterbot.corpus.english")

# Treine com base no corpus de saudações em inglês
trainer.train ("chatterbot.corpus.english.greetings")

# Treine com base no corpus de conversas em inglês
trainer.train ("chatterbot.corpus.english.conversations")


