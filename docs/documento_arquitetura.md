|Data|Versão|Descrição|Autor|
|----|------|---------|-----|
|25/09/2019|0.1|Criação do documento base|Matheus Clemente|
|17/11/2019|0.2|Tecnologias, referências e pequenas correções|Matheus Clemente|
|21/11/2019|0.3|Adição do tópico 4 (caso de uso) e respectivo diagrama|Matheus Clemente|
|24/11/2019|1.0|Especificações de caso de uso|Matheus Clemente|
---

## Documento de Arquitetura

### 1. Introdução

#### 1.1. Finalidade

<p>
Este documento visa esclarecer as decisões arquiteturais tomadas em relação ao sistema a ser produzido. Nele, procura-se ilustrar detalhes do modelo de arquitetura de software utilizado no desenvolvimento da aplicação.
</p>


#### 1.2. Escopo

<p>
Este documento de arquitetura retrata o modelo arquitetural implementado no desenvolvimento do projeto "Recomendação de Matrícula", uma extensão para o navegador Google Chrome para recomendação de matérias na plataforma Matrícula Web, com intuito de auxiliar alunos na elaboração de suas grades horárias.
</p>


#### 1.3. Definições, acrônimos e abreviações

|Sigla|Significado|
|----|------|
|HTML|Hypertext Markup Language (Linguagem de Marcação de Hipertexto)|
|CSS|Cascading Style Sheets (Folhas de Estilo em Cascata)|
|API|Application Program Interface (Interface de Programação de Aplicativos)|
|||


#### 1.4. Referências

Develop Extensions - Google Chrome. Disponível em: <https://developer.chrome.com/extensions/devguide>. Acesso em: set/2019.


#### 1.5. Visão geral

<p>
O presente documento descreve detalhadamente as características de arquitetura de software escolhidas pela equipe.
</p>

### 2. Representação da arquitetura
#### 2.1 Diagrama de relações
![Diagrama de relações da arquitetura](https://i.imgur.com/UoeLLqi.png)

<p>
O usuário interage primariamente com o site Matrícula Web, que tem sua interface alterada em pontos chave, através da extensão. O programa, por si, comunica-se com a interface HTML do site e apresenta os dados da mesma de forma personalizada ao usuário.
</p>

#### 2.2 Tecnologias 
##### 2.2.1 React (16.12.0)
<p>
Biblioteca JavaScript dedicada à criação de interfaces de usuário interativas. 
</p>

##### 2.2.2 Git (2.20.1)
<p>
Ferramenta de controle de versão de arquivos.
</p>

### 3. Objetivos e restrições da arquitetura

<p>
A seguir, estao listadas objetivos e restriçÕes do sistema relevantes à arquitetura:

- A aplicação, por se tratar de uma extensão para navegador, necessita obrigatoriamente que o usuário utilize o referido navegador (Google Chrome Versão 77.0.3865.90).
- Funciona exclusivamente no site Matrícula Web, além de depender dos dados providos por ele.
 </p>

 ### 4. Visão de casos de uso
 #### 4.1 Diagrama de caso de uso
![Diagrama de caso de uso](https://i.imgur.com/497Hh6k.png)

 #### 4.2 Especificações dos casos de uso

 |Casos de Uso|Ator|Descrição|
 |---|---|---|
 |UC01 - Acessa MatriculaWeb|Estudante|Usuário entra com seu login e senha na sua conta do MatriculaWeb. Passo necessário para acessar quaisquer dados|
 |UC02 - Acessa Quadro Resumo|Estudante|Usuário abre a página do quadro resumo para que a extensão acesse dados do fluxo do curso do aluno|
 |UC03 - Acessa Histórico Escolar|Estudante|Usuário acessa a página do histórico escolar para que a extensão acesse o histórico de matérias cursadas, e número de reprovações|
 

