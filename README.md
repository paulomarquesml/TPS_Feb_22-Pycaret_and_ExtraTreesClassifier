<h1> Introdução </h1>

<p>
<ul text="blue">
  <li text="blue">
  Competição: Tabular Playground Series - Feb 2022
  </li>
  <li>
  Foi feito com: Pycaret e Extra Trees Classifier
  </li>
  <li>
  Score: 0.97274 de 1.00000
  </li>
  <li>
  Leaderboard: 411º de 1055
  </li>
  </br>
</ul>
</p>

<h2> Detalhes da Competição </h2>
<p>
  A tarefa é classificar 10 espécies diferentes de bactérias usando os dados disponibilizados.</br>
  </br>
  As bactérias são as seguintes:</br>
  <ul>
    <li>Bacteroides Fragilis - estão frequentemente associadas a doenças no trato gastrintestinal.</li>
    <li>Campylobacter Jejuni - causa inflamação do cólon (colite) que resulta em febre e diarreia.</li>
    <li>Enterococcus Hirae - normalmente causam infecções do trato urinário, infecções pélvicas e intra-abdominais, dentre outras.</li>
    <li>Escherichia coli - pode provocar doenças, como infecções urinárias, diarreia e a colite hemorrágica e síndrome hemolítico-urêmica.</li>
    <li>Escherichia Fergusonii - pode provocar abortamento, vasculite e mamite.</li>
    <li>Klebsiella Pneumoniae - pode produzir infecções graves, como pneumonia ou meningite.</li>
    <li>Salmonella Enterica - pode causar dois tipos de doença, dependendo do sorotipo: salmonelose não tifóide e febre tifoide.</li>
    <li>Staphylococcus Aureus - causa muitos tipos de infecção, desde furúnculos até septicemias (sepse), endocardites (infecções no coração) e abscessos.</li>
    <li>Streptococcus Pneumoniae - pneumonia, meningite e otite (inflamação aguda do ouvido) são exemplos de doenças que podem ser causadas por essa bactéria.</li>
    <li>Streptococcus Pyogenes - pode provocar doenças mais graves como a escarlatina e a febre reumática.</li>
  </ul>
  </br>
</p>
<h1> Sobre o modelo </h1>
<p>Para esse modelo quis experimentar uma ferramenta que descobri recentemente, o PyCaret.
<h2> Código e Explicações PyCaret</h2>
<p>
PyCaret é uma biblioteca do Python que permite que você faça todo o ciclo da criação de um modelo de Machine Learning com poucas linhas de código.
Para começar após importar a biblioteca, criei uma variável que recebe a execução da função <i>Setup</i> responsável por inicializar o ambiente de
treinamento e criar o pipeline de transformação, essa função recebe dois parâmentros obrigatórios: data e target, podendo também receber parâmetros opcionais,
usei dois deles, um foi <i>use_gpu</i> para expecificar que quero o usar gpu.
</p>
<p>
Feito isso, usei a função <i>compare_models</i> que teina e avalia de todos os estimadores disponíveis na biblioteca de modelos usando validação cruzada.
Ainda passei uma parãmetro para a função, o <i>include=['rf', 'et', 'dt']</i> para que sejam comparados apenas os modelos que tenho interesse,
Random Forest, Extra Trees e Decision Tree. O resultado é salvo na variável <i>best</i>, agora posso executar a função <i>print(best)</i> para ver qual
o modelo que teve o melhor resultado e quais parâmetros recebeu. Nesse caso, para os dados que passei o modelo com melhor desempenho foi o Extra Trees Classifier </br>
</br>
Algo que não deixei no código final foi a função <i>evaluate_model(best)</i> que análisa o desempenho de um modelo treinado no conjunto de treino.
</p>

<h2> Código e Explicações Extra Trees Classifier</h2>
<p>
Nesse momento, peguei os parâmetros do modelo retornados e então criei o modelo agora sem pycaret utilizando os mesmos parâmetros. Separei os dados de
treino em train e test com a biblioteca <i>train_test_split</i> e começei o treino do modelo com a função <i>fit</i>. O modelo estando treinado, fiz a predição dos dados de test
com a função <i>predict</i> e o submit das predições.
</p>
<h2>Pontos</h2>
<p>
Também tentei outros parâmetros no modelo de Extra Trees. Os parâmetros do código foram os melhores que consegui.
Fiz um modelo com Random Forest que apresentou um resultado proximo desde mas este modelo ainda foi melhor.
</br>
</br>
<p>
Tem alguma dica de estudo?
Sugestão de soluções?
Vou ficar feliz com seu feedback!

Minhas redes:
<ul>
  <li>
  <a href="https://www.linkedin.com/in/paulomarquesrs1/">Linkedin</a>
  </li>
  <li>
  <a href="https://www.kaggle.com/paulomarquies">Kaggle</a>
  </li>
  <li>
  <a href="https://github.com/PauloMarquesrs">GitHub</a>
  </li>
</ul>
</p>
