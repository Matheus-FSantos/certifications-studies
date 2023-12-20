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