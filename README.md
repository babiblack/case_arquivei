# case_arquivei
Documentação da resolução do case da Arquivei

**Case Arquivei**

Elaborado em: 2021-09-20

Elaborado por: Bárbara Aires Marques

Link para o dashboard: https://drive.google.com/file/d/1tqEgQDk641ip5TVDIe9h-0lfHNypjohk/view?usp=sharing

Link para a apresentação: https://docs.google.com/presentation/d/13ZRkBSC22pNbv8QRK-JsHcx646qkIZJmiBlSDThiquk/edit?usp=sharing

---------------
**1) Base de Dados**

A base de dados fornecida contém dois arquivos CSV: customers e daily_product_usage

Conforme informado nas instruções:

"As bases irão trazer dados sobre um produto hipotético, o qual consiste em uma plataforma online com modelo de negócios em assinatura recorrente (como um Netflix ou Spotify). Seguem alguns detalhes sobre a plataforma:

- A partir do login na plataforma, o cliente dispõe de três funcionalidades para uso (funcionalidades 1, 2 e 3). Cada funcionalidade possui uma página de acesso, a partir da qual pode ser realizada alguma ação. A funcionalidade 1 possui quatro ações distintas possíveis (Ações A, B, C e D), enquanto as funcionalidades 2 e 3 possuem apenas uma ação cada.
- Ao assinar a plataforma, os usuários tornam-se clientes com status ativo, e a qualquer momento podem cancelar sua assinatura, tornando seu status inativo.
- Por ser um modelo de recorrência, a receita trazida pelos clientes é analisada de forma mensalizada, em termos de **MRR** (Monthly Recurring Revenue - receita recorrente mensal).

**1.1 Base de uso das funcionalidades (daily_product_usage)**

[Link para download da base em CSV](https://drive.google.com/file/d/1iuFvMLqzAdEsNkqxO9yanZRh12XfHz5l/view?usp=sharing) (daily_product_usage.csv)

Relação de colunas:
- Date: Data em que o cliente utilizou a funcionalidade. 	
- CustomerId: Identificador do cliente. 	
- FeatureId: Identificador da funcionalidade. 	
- DailyCount: Contagem de usos daquela funcionalidade naquele dia pelo cliente.

**1.2 Base de clientes (customers)**

[Link para download da base em CSV](https://drive.google.com/file/d/1igR2I8_c1dVZUTOj2r_04n9h6ZjYmIXP/view?usp=sharing) (customers.csv)

Relação de colunas:
- CustomerId: Identificador do cliente.
- CustomerSegment: Segmento de mercado do cliente (A, B, C, etc.). 	
- CustomerStatusToday: Status de assinatura do cliente, quando observado hoje. Pode ser Ativo (ainda é um assinante na plataforma), ou Inativo (cancelou a assinatura em algum momento). 
- CustomerMrrRange: Faixa de MRR (monthly recurring revenue - receita recorrente mensal) do cliente (baixo, médio, alto, etc.)."

--------------
**2) Confecção do case**

A análise exploratória dos dados foi realizada dentro da ferramenta Power BI, bem como o tratamento de dados e confecção de dashboards.

A apresentação com os resultados interessantes e insights concluídos a partir das análises foi confeccionada na ferramenta Google Slides.

--------------
**3) Tratamento de dados**

O tratamento dos dados foi realizado dentro da ferramenta Power BI.

Esta etapa também poderia ter sido realizada por SQL, utilizando as funções **CASE WHEN** e **DATE**. Como seria necessário fazer o upload da base de dados em uma ferramenta como Big Query ou MySQL, e visto que o PowerBI oferece essa facilidade com grande rapidez, optou-se pela última opção.

O tratamento envolveu:

**3.1 Substituição de caracteres não reconhecidos automaticamente (acentos, cedilhas, etc) pelos caracteres corretos**

Realizado pela ferramenta de Substituir Valores em Transformar Dados

**3.2 Substituição de campos nulos por "Não definido"**

Realizado pela ferramenta de Substituir Valores em Transformar Dados

**3.3 Adição de colunas segmentando ações e funcionalidades**

Realizado pela ferramenta Adicionar Coluna Condicional em Transformar Dados

**3.4 Introdução de uma tabela calendário utilizando a linguagem DAX.**

Adiciona com adição de nova tabela e input de dados com linguagem DAX, com as fórmulas CALENDAR, DAY, MONTH, YEAR e FORMAT



--------------
**4) Confecção do dashboard**

O dashboard foi elaborado através da ferramenta PowerBI. 

A visualização dos dados ocorre nas abas Overview, que mostra o perfil de usuário e os acessos globais ao longo do tempo, e a aba User Profile Over Time, que mostram os acessos ao longo do tempo dividido por drill down das categorias já apresentadas.

Também há duas abas ocultas contendo as tabelas com os principais números observados na apresentação, a fim de facilitar a obtenção de números precisos e confiáveis.

--------------
**5) Disponibilização do dashboard**

Apesar de permitido tanto para a confecção do case, como também está elencado nos conhecimentos necessários para a vaga de Product Data Analyst, o PowerBI possui a limitação de:

- Apenas permitir o compartilhamento com pessoas da mesma organização caso seja realizado dentro de uma conta corporativa gratuita;
- Impossibilidade de compartilhamento dentro de contas não corporativas (Gmail, Hotmail, etc);
- Exigência de conta Pro para compartilhamento com pessoas de fora de sua organização.

Visto isso, optou-se pelo compartilhamento do arquivo original (.pbix) publicamente através do Google Drive, permitindo que qualquer pessoa com o link possa baixar o arquivo e visualizar dentro do Power BI, que possui a licença básica gratuita tanto para Desktop quanto para Mobile.

Entende-se que, em um ambiente corporativo, haveria uma licença Pro permitindo o compartilhamento com usuários externos à organização.

--------------
**6) Apresentação**

A apresentação com os pontos mais importantes e os insights foi elaborada com a ferramenta Google Slides.

Para o design, foi utilizado um tema disponibilizado pela ferramenta e prints dos gráficos apresentados no dashboard.
