# Oracle Cloud Infrastructure Fundamentals - Course Notes
Anotações para se preparar para a certificação IZO-1085-23, certificação oficial da Oracle.


<div style="display: flex; justify-content: center">
    <img src="https://images.credly.com/images/27db49f3-8bae-4314-8a84-884935b569db/50_Oracle_Cloud_Infrastructure.png" width="200"/>
</div>

### 🧭 - Navegação:
2. OCI Overview

###
# 2. OCI Introduction

### Aula 01: Overview

**Podemos dividir a infraestrutura da Oracle Cloud em 7 categorias principais**, elas são:

1. Infrastructure;
2. Databases;
3. Data and AI;
4. Analytics;
5. Applications;
6. Governance and Administration;
7. Developer Services.

onde, cada um deles oference os respectivos serviços:

1. **Infrastructure:** Compute, Containers, OS and Vmware, Storage, Networking;
2. **Databases:** Oracle Databases, Distribuited and OSS Databases (NoSQL and MySQL);
3. **Data and AI:** Big Data, AI Services and Messaging; 
4. **Analytics:** Business Analytics;
5. **Applications:** Serverless, App Integration, Business and Industry SaaS;
6. **Governance and Administration:** Cloud Ops, Security and Observability;
7. **Developer Services:** Low Code, AppDev and Infrastruture as Code.

Essas 7 categorias e seus serviços informados são apenas alguns dos 80 serviços disponiveis na Oracle Cloud, mas tudo pode ser experimentado de graça, a Oracle contém um plano que cobra somente 1 centavo por hora (obviamente esse preço varia conforme o uso).

### Aula 02: Arquitetura da OCI.

Nessa aula será apresentado um pouco mais sobre a arquitetura da Oracle Cloud Infrastruture, que irá começar pelas ***"regiões"***.

**Regiões (Regions):** É **uma área geográfica localizada composta de** um ou mais ***domìnios de disponibilidade***.

**Domìnios de Disponibilidade (Availability Domains - "AD"):** **São**, um ou mais, **data centers tolerantes a falhas**, **localizados em uma região**, mas **conectados** uns aos outros **por uma rede de largura de banda alta** e **baixa latência**, resumidamente, eles tem as seguintes caracteristicas:

- Tolerancia a falha;
- Localizados em uma região;
- Conectados por uma rede de largura de banda alta;
- e Baixa latência.

**Dominios de Falha (Fault Domains - FD):** São **um agrupamento de hardware e infraestrutura dentro de um dominio de disponibilidade** para fornecer antiafinidade. Pode ser pensado como *data centers lógicos.*


> **Como escolher uma região?** </br>
 Para escolher uma região primeiro você deve escolher a que está mais próximo dos seus usuários, para uma latencia menor e mais performance. </br></br>
 O segundo critério são os "requisitos de residencia e conformidade de dados". Muitos países têm requisitos rigorosos de residência de dados e você deve cumprir com eles. Portanto, escolha uma região com base nesses requisitos de conformidade. </br></br>
 E por fim, deve-se levar em conta a disponibilidade do serviço. Novos serviços em nuvem são disponibilizados com base na demanda regional, por motivos de conformidade regulatória, com disponibilidade de recursos e vários outros fatores. </br></br>
 Tenha sempre esses 3 critérios para escolher uma região.

#

### Mais sobre cada um

**AD:** Os *ADs* são isolados um dos outros, tolerantes a falhas e improvável que falhem simultaneamente (por não compartilharem uma infraestrutura fisica, é improvavel que uma falha em um AD impacte nos outros, como na foto abaixo).

![Dominios de disponibilidade](image.png)

> Obs.: Cada dominio de disponibilidade (AD) tem 3 dominios de falha (FD), como na foto abaixo.

![3 dominios de disponibilidade com 3 dominios de falha para cada](image-1.png)

**FD:** São "data centers lógicos" dentro dos *ADs*. A idéia é que você coloque os recursos em diferentes dominios de falha (FD) e eles não compartilham um unico ponto de falha de hardware (como servidores fisicos, switcges, rack fisico e etc.) como na imagem abaixo.

![2 dominios de falha funcionando e 1 com falha](image-2.png)

Fazendo isso, você pode obter mais disponibilidade, e aproveitará os FDs corretamente, é claro.

Mas qual seria a recomendação? A recomendação é que temos essas contruções, como dominios de falha e dominios de disponibilidade, nos ajudam a evitar pontos únicos de falha. Portanto, garantimos que tudo seja redundate e com isso, então, caso tenhamos falhas de hardware, diminuimos essas falhas ao máximo possivel.
