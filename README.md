# Kaggle-House-Prices
Repository for the shared development of the open competition House Prices on the Kaggle platform

# Resumo dos passos percorridos e conclusão
Neste tópico, iremos descrever de forma breve todos os testes desenvolvidos e a metodologia de trabalho. A cima de cada função, é possivel encontrar sua descrição e como as implementamos.

* Iniciamos nosso trabalho sumerizando os dados categoricos. Implementamos uma versão manual do label_encoder, uma para o one_hot_encoder e uma hibrida convertendo apenas categoricos com 4 ou menos campos.

* Nosso primeiro desafio foi "tapar" os buracos deixados pela falta de dados (objetos .nan). Tentamos diversas metodologias, por exemplo, inserir a média dos dados, maximos, minimos, constante 0 e por fim a utilização do algoritmos KNN como auxilio.

* Logo partimos para a compreenção dos dados, onde plotamos dois tipos de gráficos, o histograma e o gráfico boxplot. Eles foram extremamente uteis para a compreenção dos dados numéricos.

* Mesmo sem remover colunas ou adicionar novas features, fomos direto a implementação dos preditores, onde testamos diversos modelos. Percebemos que ao utilizar o label_encoder a precisão era em torno de 90% para o xgboost. 

* Nosso próximo desafio foi tentar detectar outliers, esta tarefa foi a mais dificil e de fato nós não conseguimos no sair bem nela. Identificamos diversos outliers e tentamos diversas abordagens como a remoção de linhas, colunas e etc. Mas todas causavam impacto negativo no nosso modelo. Foi então que resolvemos buscar um recurso da estatistica chamado boxplot, com ele nós conseguimos "remodelar" os dados de forma que ficassem dentro da box. Outra abordagem foi a transformação dos dados numéricos para log. A mistura dos dois recursos foi bastante benefica para algumas colunas e nos trouxe aproximadamente cerca de + 2% na precisão.

* Em seguida adicionamos uma função que remove uma coluna e verifica a precisão do modelo. Ela foi extremamente util para sabermos qual coluna não alterava os dados ou causava impacto negativo ao resultado final.

* Tentamos de diversas formas adicionar novas features relacionando colunas. E isto foi bastante promissor, conseguimos adicionar varias colunas que trouxeram um impacto positivo.

* Após diversas falhas e exitos fomos a uma implementação mais robusta do modelo escolhido, onde percorremos diversos parametros para ele e verificamos qual era mais benefico para nosso modelo final. 

* O score final foi de 93.35%, embora nos acreditemos que ainda seja possivel melhorar e muito esse score, estamos satisfeitos, pois conseguimos trabalhar com diversos recursos e técnicas de engenharia de atributos. Percebemos que é bastante desafiador encontrar novos dados atraves dos já existentes e principalmente detectar outliers, o que de fato nos deu muita dor de cabeça, mas não é algo impossivel.

* Resultado final:
 Score: 0.13045
 Posição: 1281 / 4454
 
 
