# Sistema de Recomendação para uma Empresa de Varejo
****

## 🔍 Sobre o Projeto

O objetivo deste projeto é desenvolver um Sistema de Recomendação que indique clientes e produtos parecidos, afim de que seja possível realizar promoções personalizadas para os clientes de uma empresa de varejo. O tipo de Sistema de Recomendação que utilizei foi o de Filtragem Colaborativa (Collaborative Filtering). E o algoritmo utilizado no Sistema de Recomendação foi o de Similaridade de Cossenos.

Esse tipo de trabalho em dados é muito interessante por **desmistificar** a ideia geral que se tem de que apenas empresas gigantes, como Netflix e Amazon, podem ter um Sistema de Recomendação para os seus clientes. Na verdade, **qualquer empresa** com informações a respeito das compras realizadas pelos seus clientes **pode ter o seu próprio Sistema de Recomendação** e se beneficiar comercialmente com a sua utilização.

O projeto foi desenvolvido em Jupyter Notebook. Todo o trabalho foi elaborado a partir de um dataset de cerca de 407 mil linhas com diversos pedidos realizados por clientes em diferentes países. 

A base de dados foi buscada do Kaggle:

Título: Online Retail Data Set

URL [https://www.kaggle.com/datasets/vijayuv/onlineretail]

## 🗃️ Etapas do Projeto

Para o desenvolvimento do projeto foram importadas e utilizadas várias bibliotecas, como pandas, numpy e scikit-learn.

Foi elaborada a fase de Preparação de Dados, em que agrupei em um DataFrame a quantidade total vendida de cada produto para cada cliente.

Em seguida, utilizei o algoritmo cosine_similarity da biblioteca scikit-learn, que mede a semelhança entre dois vetores com base no ângulo entre eles. Quanto mais próximo de 1 for o cosseno desse ângulo, maior a similaridade entre os vetores. Esse algoritmo foi utilizado tanto para avaliar os clientes mais parecidos entre si quanto os produtos mais similares.

Por fim, elaborei 2 funções:

1) Função nomeada de 'clientes_similares': Ela recebe parâmetros referentes a um cliente em específico. E retorna um Dataframe com os clientes mais similares ao cliente informado na função, o nível % de similaridade e 3 produtos que cada um dos clientes similares comprou que o cliente informado na função não comprou. Esse retorno é bastante útil para qualquer área comercial, uma vez que recomenda outros clientes parecidos ao cliente em questão e potenciais novos produtos que ele provavelmente vai se interessar em adquirir.

2) Função nomeada de 'produtos_similares': Ela recebe parâmetros referentes a um produto em específico. E retorna um DataFrame com os produtos mais similares ao produto informado e o nível % de similaridade desses produtos com o produto informado. O retorno dessa função também é bastante útil já que recomenda produtos similares a um determinado produto que um cliente se interessou, aumentando o potencial de vendas.
