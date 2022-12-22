Criação de um banco de tweets rotulados como "não ofensivo",  "ofensivo" ou "discursos de ódio".
Paola Silva de Almeida  (bolsista PROEX) -  paola_almeida@id.uff.br  
Jessica Quintanilha Kubrusly  (orientadora) -  jessicakubrusly@id.uff.br 
Karina Yuriko Yaginuma (orientadora) -  karinayuriko@id.uff.br
 
Departamento de Estatística
Instituto de Matemática e Estatística
Universidade Federal Fluminense
Resumo
Este texto trás alguns critérios usados para produzir o banco de tweets registrados neste artigo.
Metodologia:
                As pesquisas foram separadas em cinco grandes
temas: homofobia, misoginia, xenofobia,
intolerância religiosa e  racismo.
Para cada tema foi feita uma busca. Essa busca é feita a partir da função get_all_tweets do pacote academictwittweR (Barrie and Ho 2021), que recebe como
entrada um texto composto por palavras chaves e retorna um banco de dados com
os textos encontrados no período de tempo estipulado, que contenham as palavras
chaves utilizadas na busca. 
                Para
criar o texto de entrada com as palavras chaves foi utilizada a seguinte
metodologia. Para cada tema foram escolhidos alguns pronomes e alguns Adjetivos
/Insultos, referentes ao tema em questão. Em seguida foi criado um texto
composto por todas as combinações entre os pronomes e os adjetivos / insultos. 
Por exemplo, veja na Tabela abaixo, o primeiro tema é sobre
Intolerância religiosa, primeira linha. Para esse tema os pronomes escolhidos
estão apresentados na segunda coluna e os adjetivos na terceira. Combinando
todas as possibilidades, o texto de busca para esse tema foi: “macumbeiro tem
que morrer”, “macumbeiro de merda”, …, “crente tem que morrer”, “crente de
merda”, … “mulçumano raça ruim”. O período de busca para cada tema e o número
de textos encontrados também estão presentes na Tabela 1.
 
Tabela 1: Descrição do método de busca pelos tweets
 
Tema
	Pronomes 
	Adjetivos / Insultos
	Período
	Nº de 
textos 
	Intole-
rância religiosa
	"macumbeiro", "crente", "católico", "marçonaria", "judeu", "mulçumano"
	“tem que morrer", "de merda", "vai pro inferno", "porco", "tudo safado", "fudido", "raça ruim"
	20/01/22 
a
30/08/22
	6.927
	xenofobia
	"nordestino", "paraíba", "sulista", "carioca", "venezuelano", "chinês"
	"tem que morrer", "de merda", "volta seu país", "porco", "tudo","fudido", "raça ruim"
	20/01/22
a
30/08/22
	9.915
	racismo
	"preto", "preta", "neguinho", "neguinha", "mulata", "mulato"
	"tem que morrer", "bandido", "macaco", "macaca", "escrota", "fudido", "fudida", "raça ruim"
	20/01/22
a
30/08/22
	9.646
	homofobia
	"sapatão", "viadinho", "bichinha", "traveco", "mulher macho", "trans"
	"tem que morrer",  "safado", "safada", "pecado", "escrota", "não é normal", "ta errado"
	20/01/22
a
30/08/22
	8.424
	misoginia
	"mulher", "garota", "menina"
	"vadia", "vadi@", "v@di@", "v@dia", "puta", "put@", "vagabunda", "v@g@bund@", "vagabund@", "interesseira", "provocou", "provoca", "piranha", "piranh@", "poço de esperma", "burra", "burr@", “incopetente"
	20/01/22
a
28/08/22
	9.819
	 
 
Tabela 2: Descrição das variáveis da base de dados
Nome
	Tipo
	Descrição
	Tweet
	Texto
	O texto escrito por algum usuário no Twitter.
	Tema
	Categórica
	Uma entre as 5 possibilidade: Intolerância religiosa, xenofobia, racismo, homofobia ou misoginia
	Tipo
	Categórica
	Um rótulo associado a cada twiite, feito manualmente, podem ser: não ofensivo, ofensivo ou discurso de ódio.
	ID do usuário
	Numérica
	Código numérico que identifica o usuário que escreveu o tweet.
	Resposta
	Lógica
	Indica se o tweet é uma resposta para a postagem de outro usuário ou não.
	ID resposta
	Numérica
	Código numérico que identifica o usuário que recebeu o tweet em questão como resposta, se for o caso. 
	Dispositivo
	Categórica
	Tipo de dispositivo usado para a postagem. 
	Data
	Data 
	Data em que o texto foi postado.
	Hora
	Hora
	Hora que o texto foi postado. 
	 
Conclusão:
Ao todo foram coletados 44.731 tweets que estão reunidos em um único arquivo intitulado BASE DISCURSO DE ÓDIO. Seguindo o princípio FAIR em Ciências de Dados, apresentado por Mondelli et al (Mondelli, Peterson, and Gadelha 2019).Todo o script utilizado para criar este banco de tweets está disponível em: https://github.com/paola-almeida/script-banco-de-dados.git