**UGV – Centro Universitário**

Curso Bacharelado em Engenharia de Software – 4º Período

**TRILEDU**

Plataforma de Gestão Escolar

**DOCUMENTO DE VISÃO**

Ana Vitória Basniak

Felipe Bernardino Silva

Gabriel Henrique Libmann

Igor Andriel Hetman

Luana Gabrielly Pszymus

Natali Lascoski

Rafael Roiek Correa

União da Vitória – PR

06 de junho de 2025 (revisado em outubro de 2026)

*Status do projeto: fase de documentação e prototipação. O software ainda não foi desenvolvido.*


# 1\. Introdução

## 1.1 Propósito

O presente documento tem como propósito descrever a visão geral da plataforma Triledu, voltada à gestão escolar, especificando seus objetivos, escopo, usuários envolvidos e restrições iniciais. Este documento servirá como guia para todos os stakeholders do projeto, incluindo equipe técnica, gestores, professores, alunos e responsáveis, fornecendo um entendimento comum sobre o sistema que será construído.

## 1.2 Escopo

A plataforma de gestão escolar tem como escopo principal integrar, em um único ambiente digital, os processos administrativos, pedagógicos e comunicacionais de uma instituição de ensino. O sistema contemplará módulos para cadastro de alunos, turmas e professores, gestão de notas e frequência, comunicação entre escola e responsáveis, emissão de relatórios e acompanhamento do desempenho escolar. O projeto busca reduzir a burocracia, aumentar a eficiência da gestão e melhorar a interação entre os diferentes perfis de usuários.

Situação atual: até esta data foram produzidos o Documento de Visão, a modelagem UML e protótipos de tela. A implementação do software ainda não foi iniciada.

## 1.3 Definições, acrônimos e abreviações

- SGE – Sistema de Gestão Escolar.

- Stakeholder – Parte interessada no projeto (usuário final, cliente, gestor ou equipe técnica).

- RF – Requisitos Funcionais.

- RNF – Requisitos Não Funcionais.

- RA – Registro Acadêmico.

- MEC – Ministério da Educação.

- EAD – Ensino a Distância.

- TI – Tecnologia da Informação.

- PDF – Portable Document Format (formato de documento portátil).

- LGPD – Lei Geral de Proteção de Dados (Lei nº 13.709/2018).

- ECA – Estatuto da Criança e do Adolescente (Lei nº 8.069/1990).

- ISO, CMM, UL – Padrões de qualidade e segurança internacionais.

- TCP/IP, ISDN – Padrões de comunicação de rede.

- Banco de dados – Local onde ficam armazenadas as informações.

- Back-end – Parte “invisível” do sistema, responsável pela lógica e pelo banco de dados.

- Front-end – Parte “visível” do sistema, interface usada pelos usuários.

- Scripts – Pequenos programas usados para automatizar tarefas.

- Validação de dados – Conferência automática para evitar erros ou duplicações de informações.

- Backup – Cópia de segurança dos dados.

- Logs – Registros automáticos de atividades do sistema.

## 1.4 Referências

- PRESSMAN, Roger S.; MAXIM, Bruce R. Engenharia de software. Grupo A, 2021. E-book. ISBN 9786558040118.

- RUBIN, Kenneth S. Scrum essencial: um guia prático para o mais popular processo ágil. Alta Books, 2017. E-book. ISBN 9788550804118.

- LEDUR, Cleverson L. Análise e Projeto de Sistemas. Grupo A, 2018. E-book. ISBN 9788595021792.

- LARMAN, Craig. Utilizando UML e Padrões: uma introdução à análise e ao design orientados a objetos e ao desenvolvimento iterativo. 3. ed. Porto Alegre: Bookman, 2007.

- WAZLAWICK, Raul Sidnei. Análise e design orientados a objetos para sistemas de informação. 2. ed. Rio de Janeiro: Elsevier, 2014.

- GAUSE, Donald; WEINBERG, Gerald. Exploring Requirements: Quality Before Design. New York: Dorset House, 1989.

- LEVY, Jaime. Estratégia de UX: técnicas de estratégia de produto para criar soluções digitais inovadoras. 2. ed. São Paulo: Novatec, 2023.

- OLIVEIRA, Cláudio Luís V.; ZANETTI, Humberto Augusto P. Javascript descomplicado: programação para web, IoT e dispositivos móveis. Saraiva, 2020. E-book. ISBN 9788536533100.

- IEPSEN, Edécio Fernando. Lógica de programação e algoritmos com JavaScript. 2. ed. São Paulo: Novatec, 2022.

- SILVA, Luiz F. C.; RIVA, Aline D.; ROSA, Gabriel A.; et al. Banco de Dados Não Relacional. Grupo A, 2021. E-book. ISBN 9786556901534.

- SILBERSCHATZ, Abraham. Sistema de Banco de Dados. Grupo GEN, 2020. E-book. ISBN 9788595157552.

- PICHETTI, Roni F.; VIDA, Edinilson S.; CORTES, Vanessa S. M. P. Banco de dados. Grupo A, 2021. E-book. ISBN 9786556900186.

## 1.5 Visão geral

Este documento está estruturado para fornecer uma visão completa do sistema de gestão escolar. A Seção 2 apresenta o posicionamento do produto, incluindo os problemas atuais e a justificativa para a criação do sistema. A Seção 3 descreve os stakeholders e perfis de usuários. A Seção 4 detalha a visão geral do produto. A Seção 5 lista os recursos (requisitos) e traz os diagramas e protótipos. As Seções 6 e 7 tratam das restrições e das faixas de qualidade. As Seções 8 a 12 abordam precedência e prioridade, outros requisitos, documentação, atributos dos recursos e cronograma.

# 2\. Posicionamento

## 2.1 Oportunidade de negócios

A melhoria contínua dos sistemas de gestão escolar passa pela análise detalhada dos desafios e limitações das soluções atuais. Identificar os problemas existentes permite desenvolver estratégias eficazes para otimizar o desempenho do sistema, tornando-o mais eficiente e alinhado às necessidades das instituições de ensino. Com o crescimento do setor educacional, impulsionado pela expansão de escolas, cursos e faculdades, nas modalidades presencial e a distância (EAD), é essencial contar com um sistema de gestão capaz de integrar e oferecer os serviços tecnológicos necessários. Dessa forma, a modernização dessas plataformas contribui para uma gestão mais ágil, organizada e inovadora.

## 2.2 Instrução do problema

A gestão eficiente de uma instituição de ensino depende diretamente da confiabilidade e da usabilidade de seu sistema de gestão escolar. No entanto, muitas plataformas enfrentam desafios que comprometem seu desempenho e prejudicam as atividades acadêmicas e administrativas. Falhas recorrentes e avarias estão entre os problemas mais críticos, afetando a estabilidade da plataforma e interrompendo o fluxo de trabalho de alunos, professores e gestores.

Além da instabilidade, a usabilidade também é um obstáculo. Interfaces pouco intuitivas dificultam a navegação e exigem tempo de adaptação prolongado. O problema se agrava quando a falta de suporte técnico ágil impede a rápida resolução de dificuldades, prolongando períodos de inatividade e frustrando os usuários.

Outro desafio relevante é a limitação de acesso por dispositivos móveis. Em um cenário em que a mobilidade é essencial para a rotina acadêmica, a falta de compatibilidade com smartphones e tablets restringe o acompanhamento de informações por professores, alunos e responsáveis. Além disso, a dificuldade em localizar documentos e registros acadêmicos compromete a organização dos processos escolares, tornando as tarefas rotineiras mais demoradas e burocráticas.

Diante desses desafios, torna-se essencial desenvolver uma solução que garanta estabilidade e bom funcionamento e que ofereça uma experiência intuitiva e acessível, com melhorias na interface, suporte técnico eficiente e integração com dispositivos móveis, construindo um ambiente digital mais moderno, ágil e alinhado às necessidades educacionais atuais.

## 2.3 Instrução de posição do produto

Para as instituições de ensino, o Triledu é uma plataforma digital de gestão escolar que oferece interface intuitiva, compatibilidade com dispositivos móveis e automação de processos essenciais, garantindo maior eficiência e acessibilidade em comparação com os sistemas atuais.

# 3\. Descrições da Parte Interessada e do Usuário

## 3.1 Demográficos de mercado

A adoção de plataformas de gestão escolar tem apresentado crescimento significativo, impulsionada pela necessidade de modernização dos processos administrativos e acadêmicos e pela busca por soluções eficazes de comunicação entre escolas, alunos e responsáveis. O projeto busca atender a uma demanda clara e crescente do setor educacional, contemplando instituições públicas e privadas.

O público-alvo é composto por gestores escolares, professores, responsáveis legais e alunos, sem distinção de gênero. A faixa etária é variada: profissionais da secretaria e gestores entre 25 e 60 anos, professores entre 22 e 55 anos, responsáveis entre 25 e 50 anos e alunos entre 6 e 18 anos na educação básica, podendo chegar a 24 anos no ensino técnico.

Quanto à escolaridade, gestores e profissionais da secretaria geralmente possuem ensino superior completo ou em andamento (Administração, Pedagogia ou afins); os professores possuem licenciatura; os responsáveis têm, em sua maioria, ensino médio ou superior completo; e os alunos cursam o ensino fundamental, médio ou técnico.

A renda familiar varia conforme o tipo de instituição: nas escolas privadas, a renda média situa-se entre três e dez salários mínimos; nas públicas, é mais diversificada, geralmente entre um e cinco. O público concentra-se em áreas urbanas e suburbanas, com maior acesso à internet e a tecnologias móveis, havendo perspectiva de expansão para regiões semiurbanas. A maioria dos usuários tem alto acesso a dispositivos móveis e computadores e habilidades digitais em nível básico a intermediário, o que exige uma plataforma intuitiva, de fácil utilização e com interface acessível.

O mercado educacional brasileiro oferece um cenário promissor. Segundo dados do INEP citados pela equipe, existem no país mais de 180 mil instituições de ensino e aproximadamente 47 milhões de estudantes. (Recomenda-se, antes da publicação, confirmar esses números e citar a fonte e o ano do levantamento.) A tendência é de continuidade do crescimento do mercado de tecnologia educacional, acentuado no período pós-pandemia, com potencial para atender diretamente mais de 20 mil instituições privadas e impactar o setor público por meio de parcerias ou soluções adaptadas. As tendências mais relevantes incluem a digitalização de processos escolares, o aumento de investimentos em tecnologias de gestão educacional e a demanda por plataformas responsivas com comunicação integrada.

Quanto à reputação, por se tratar de uma solução em desenvolvimento, a imagem no mercado ainda está sendo construída; a intenção é posicioná-la como moderna, acessível, confiável e intuitiva. Existem plataformas consolidadas, como SAE Digital, Sponte e Escolaweb, reconhecidas por sua robustez, mas há relatos de insatisfação com a complexidade de uso, a falta de flexibilidade para instituições menores, os altos custos e a demora no suporte. A proposta é oferecer uma alternativa que se destaque pela simplicidade, suporte eficiente, preço competitivo e capacidade de adaptação a instituições de diferentes portes, de pequenas escolas a grandes redes. Assim, o produto contribui para os objetivos estratégicos da organização ao promover a inovação no setor educacional, simplificar a gestão acadêmica, aumentar a produtividade administrativa e fortalecer a comunicação com a comunidade escolar.

## 3.2 Resumo da parte interessada

| **Nome**                      | **Representa**                                                                                                                                              | **Função**                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Equipe de Desenvolvimento     | Ana Vitória Basniak, Felipe Bernardino Silva, Gabriel Henrique Libmann, Igor Andriel Hetman, Luana Gabrielly Pszymus, Natali Lascoski e Rafael Roiek Correa | Projetar, documentar, desenvolver (front-end, back-end e banco de dados), testar e entregar a aplicação. |
| Profissional da Educação      | Consultoria pedagógica do projeto                                                                                                                           | Orientar processos educacionais, validar requisitos pedagógicos e apoiar os testes de usabilidade.       |
| Direção Escolar / Mantenedora | Equipe diretiva e administrativa da instituição                                                                                                             | Definir o escopo, validar funcionalidades e analisar resultados e indicadores.                           |
| Secretaria Escolar            | Profissionais administrativos da instituição                                                                                                                | Participar do levantamento de requisitos e da homologação das funcionalidades administrativas.           |
| Coordenação de Suporte        | Equipe de atendimento aos usuários                                                                                                                          | Atender chamados, orientar o uso, registrar ocorrências e produzir materiais de apoio.                   |

## 3.3 Resumo do usuário

| **Nome**           | **Descrição**                                                                                              | **Parte interessada**         |
|--------------------|------------------------------------------------------------------------------------------------------------|-------------------------------|
| Professor          | Lança chamadas, notas e avaliações, publica atividades e planos de aula e se comunica com os responsáveis. | Direção Escolar / Mantenedora |
| Aluno              | Consulta boletim, calendário, frequência, materiais e comunicados; envia tarefas.                          | Direção Escolar / Mantenedora |
| Responsável        | Acompanha boletim, frequência, avisos e eventos; mantém dados atualizados.                                 | Direção Escolar / Mantenedora |
| Secretaria Escolar | Gerencia matrículas, turmas, documentos, frequência e comunicação institucional.                           | Secretaria Escolar            |
| Gestor Escolar     | Acompanha indicadores, supervisiona processos e gera relatórios gerenciais.                                | Direção Escolar / Mantenedora |
| Equipe Técnica     | Desenvolve, testa, corrige e evolui a plataforma.                                                          | Equipe de Desenvolvimento     |
| Equipe de Suporte  | Atende usuários, registra ocorrências e mantém a base de conhecimento.                                     | Coordenação de Suporte        |

## 3.4 Ambiente do usuário

- **Quantas pessoas estão envolvidas na tarefa? Está sendo alterado?** Atualmente, a equipe de desenvolvimento (sete integrantes) e uma profissional da educação. Não houve alterações neste grupo até o momento.

- **Quanto tempo leva um ciclo de tarefa?** As atualizações do projeto são realizadas quinzenalmente; cada ciclo de atividade segue esse intervalo.

- **Quais restrições de ambiente afetam o projeto?** Não há restrições no momento. Os integrantes atuam de forma remota ou presencial, conforme a necessidade.

- **Quais plataformas de sistema estão em uso? Há plataformas futuras planejadas?** Nenhuma plataforma está em uso; o projeto está em fase inicial. Está planejada uma aplicação web responsiva, com possível versão em aplicativo móvel (Android e iOS).

- **Que outros aplicativos estão em uso? É necessária integração?** Não há uso de outros aplicativos nem necessidade de integração neste momento. Integrações futuras estão descritas na seção 4.1.

## 3.5 Perfis das partes interessadas

| **Representante**        | **Tipo / Atuação**                                            | **Responsabilidades**                                                                           | **Critérios de sucesso e desafios**                                                                                                                                           |
|--------------------------|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Luana Gabrielly Pszymus  | Equipe de desenvolvimento – front-end e documentação técnica  | Implementar a interface e organizar a documentação de uso da aplicação.                         | Sucesso: alto nível de usabilidade e acessibilidade plena. Desafios: prazos curtos para testes, ajustes rápidos e alinhamento constante com a equipe.                         |
| Ana Vitória Basniak      | Equipe de desenvolvimento – documentação e apoio ao front-end | Elaborar a documentação técnica e apoiar a implementação da interface.                          | Sucesso: documentação correta, completa e alinhada à aplicação. Desafios: alinhar documentação e desenvolvimento em prazos curtos; revisão técnica constante.                 |
| Gabriel Henrique Libmann | Equipe de desenvolvimento – back-end e front-end              | Programar as funcionalidades e integrar as camadas da aplicação.                                | Sucesso: estrutura de programação correta e funcional, conforme os requisitos. Desafios: conciliar prazos curtos e complexidade; testes frequentes na integração.             |
| Igor Andriel Hetman      | Equipe de desenvolvimento – back-end e front-end              | Programar as funcionalidades e integrar as camadas da aplicação.                                | Sucesso: estrutura de programação correta e funcional, conforme os requisitos. Desafios: conciliar prazos curtos e complexidade; testes frequentes na integração.             |
| Natali Lascoski          | Equipe de desenvolvimento – back-end e banco de dados         | Modelar, estruturar e manter o banco de dados com armazenamento seguro e eficiente.             | Sucesso: banco de dados correto, com desempenho e integridade. Desafios: grande volume de dados, desempenho das consultas e compatibilidade entre camadas.                    |
| Rafael Roiek Corrêa      | Equipe de desenvolvimento – back-end                          | Desenvolver a estrutura funcional e a integração com o banco de dados.                          | Sucesso: funcionalidades completas e sistema em pleno funcionamento. Desafios: correção de falhas em tempo hábil, integração entre módulos e estabilidade nos testes.         |
| Felipe Bernardino Silva  | Equipe de desenvolvimento – back-end e banco de dados         | Desenvolver a lógica do sistema e modelar/manter o banco de dados.                              | Sucesso: funcionalidades e estrutura de dados completas, com integridade e desempenho. Desafios: dados complexos, integração entre camadas e limitações de tempo para testes. |
| Profissional da Educação | Apoio pedagógico                                              | Orientar processos educacionais, colaborar nas funcionalidades pedagógicas e validar conteúdos. | Sucesso: adequação do sistema às rotinas educacionais. Desafios: alinhar necessidades pedagógicas e soluções tecnológicas; clareza na comunicação entre áreas.                |

*Observação: nos perfis originais, os integrantes da equipe eram classificados como “administrador(a) de sistema”. Como esse termo designa um perfil de uso da plataforma, optou-se por descrever o papel de cada integrante na equipe de desenvolvimento.*

## 3.6 Perfis do usuário

| **Usuário**        | **Tipo e responsabilidades**                                                                                                  | **Critérios de sucesso**                                                                         | **Envolvimento, entregas e desafios**                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Professor          | Intermediário a especialista. Registra chamadas, lança notas e avaliações, atualiza conteúdos e comunica-se com responsáveis. | Facilidade e agilidade nas tarefas; economia de tempo e melhor organização e comunicação.        | Valida requisitos e testa usabilidade. Entrega relatórios de desempenho, notas e chamadas. Desafios: adaptação a novas tecnologias, interfaces intuitivas e proficiência digital variável (pode exigir treinamento).          |
| Aluno              | Novato a intermediário. Consulta boletins, calendário, materiais, atividades e comunicados; envia tarefas.                    | Facilidade de acesso e clareza da interface; autonomia para acompanhar o desempenho.             | Testes de usabilidade e feedback. Entrega tarefas pelo sistema. Desafios: pouca familiaridade digital (mais jovens) e limitações de internet ou dispositivos.                                                                 |
| Responsável        | Novato. Acompanha boletins, frequência, avisos, eventos e andamento pedagógico; mantém dados atualizados.                     | Transparência, navegação simples e rapidez nos comunicados; confiança no acompanhamento escolar. | Uso contínuo e sugestões. Entrega confirmações de leitura e atualização de cadastros. Desafios: baixa familiaridade, dificuldades de login e necessidade de interface extremamente simples.                                   |
| Secretaria Escolar | Intermediário. Gerencia matrículas, turmas, documentos, frequência e comunicação institucional.                               | Eficiência, automação de tarefas repetitivas e confiabilidade dos dados.                         | Participa do levantamento de requisitos à homologação. Entrega certificados, históricos, relatórios de matrícula e frequência. Desafios: relatórios personalizados, fluxos automatizados e integração com processos internos. |
| Gestor Escolar     | Especialista. Acompanha indicadores, supervisiona processos, valida informações e gera relatórios.                            | Relatórios claros, dashboards rápidos e segurança dos dados.                                     | Define escopo e valida funcionalidades. Entrega relatórios gerenciais e dashboards. Desafios: informações consolidadas e flexíveis, filtros, exportação e visualização analítica.                                             |
| Equipe Técnica     | Especialista. Desenvolve, testa e corrige; implementa melhorias e garante a estabilidade.                                     | Qualidade técnica, desempenho, tempo de resposta e ausência de erros críticos.                   | Presente da concepção à entrega contínua. Entrega releases, documentação técnica, logs e scripts. Desafios: mudanças de escopo sem aviso, ambientes de teste incompletos e pouco feedback dos usuários.                       |
| Equipe de Suporte  | Técnico-intermediário. Atende chamados, esclarece dúvidas, encaminha erros e produz materiais de apoio.                       | Menor tempo de resposta, alta resolução no primeiro contato e satisfação do usuário.             | Entra nas fases de testes e segue na operação. Entrega relatórios, estatísticas, tutoriais e base de conhecimento. Desafios: falta de documentação, treinamentos limitados e poucos recursos para casos complexos.            |

## 3.7 Principais necessidades da parte interessada ou do usuário

| **Problema**                                 | **Motivo**                                         | **Solução atual**                           | **Solução desejada**                                             | **Imp. (1–5)** | **Prioridade** |
|----------------------------------------------|----------------------------------------------------|---------------------------------------------|------------------------------------------------------------------|----------------|----------------|
| Comunicação pais/escola                      | Dificuldade na troca de informações claras         | Avisos impressos ou comunicados esporádicos | Canal digital direto e acessível entre pais e escola             | 5              | Alta           |
| Integração das atividades pedagógicas        | Atividades em diferentes plataformas               | Organização manual                          | Sistema unificado com calendário e gerenciamento de atividades   | 4              | Alta           |
| Interface e conexão afetam o uso             | Interface pesada e dependência de boa conexão      | Interface web sem otimização                | Interface leve e responsiva, com modo offline para instabilidade | 4              | Média          |
| Padrão MEC e interoperabilidade              | MEC exige integração e envio de dados padronizados | Exportação manual de dados                  | Compatibilidade com padrão MEC e exportação automática           | 5              | Alta           |
| Sobrecarga do servidor em horários de pico   | Muitos acessos simultâneos                         | Recarregamento manual                       | Escalabilidade automática e balanceamento de carga               | 4              | Alta           |
| Acesso às notas por app ou site              | Falta de centralização e login instável            | Notas em boletins físicos                   | Consulta de notas via app/site com autenticação segura           | 5              | Alta           |
| Notificação de desempenho aos pais           | Comunicação falha sobre rendimento                 | Relatórios periódicos em papel              | Notificações automáticas com desempenho e alertas personalizados | 4              | Média          |
| Evasão escolar e comunicação com base no ECA | Escola não informa imediatamente os responsáveis   | Monitoramento por planilhas                 | Alerta automático sobre faltas para pais e conselhos tutelares   | 5              | Alta           |
| Compatibilidade entre sistemas               | App otimizado apenas para um sistema               | Funciona parcialmente em ambos              | Aplicativo totalmente compatível com Android e iOS               | 4              | Média          |

## 3.8 Alternativas e concorrência

| **Alternativa**                              | **Descrição**                                         | **Pontos fortes**                                                           | **Pontos fracos**                                                                       |
|----------------------------------------------|-------------------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Sponte                                       | Gestão educacional com foco em escolas particulares   | Interface moderna, controle de frequência, notas, financeiro, app para pais | Custo elevado, pouco personalizável, suporte limitado a escolas públicas                |
| SAE Digital                                  | Solução voltada à gestão pedagógica integrada         | Conteúdo alinhado à BNCC, integração com ensino híbrido                     | Foco mais pedagógico que administrativo; menos recursos de gestão escolar               |
| i-Educar (open source)                       | Sistema público gratuito para gestão escolar          | Código aberto, personalizável, sem custo de licença                         | Exige equipe técnica, curva de aprendizado, atualizações manuais                        |
| Google Workspace for Education               | Ferramentas Google aplicadas ao ambiente escolar      | Gratuito para instituições, fácil adoção, conhecido pelos professores       | Não é um sistema de gestão completo; depende de configurações paralelas                 |
| Desenvolvimento interno                      | Sistema sob medida feito pela própria instituição     | Controle total dos requisitos e adaptação plena                             | Alto custo e tempo de desenvolvimento; manutenção contínua                              |
| Moodle com extensões                         | Plataforma educacional adaptável com plugins          | Flexível, bem documentada, gratuita                                         | Exige personalização, pouco intuitiva, foco principal em EAD                            |
| TOTVS – Linha Educacional                    | Solução robusta para instituições públicas e privadas | Módulos integrados de matrícula, notas, financeiro, biblioteca etc.         | Custo alto, curva de aprendizado longa, excesso de funcionalidades para escolas menores |
| Manter o status atual (planilhas e cadernos) | Documentos físicos e digitais não integrados          | Nenhum custo adicional; familiaridade com o processo                        | Falta de integração, risco de perda de dados, dificuldade de comunicação e controle     |

# 4\. Visão Geral do Produto

Esta seção apresenta uma visão de alto nível das capacidades do sistema, seu posicionamento em relação a outros sistemas, suas principais funções e as condições que afetam seu funcionamento.

## 4.1 Perspectiva do produto

O sistema de gestão escolar é uma aplicação web responsiva, acessível em navegadores e dispositivos móveis, projetada para centralizar as operações administrativas, pedagógicas e de comunicação em uma única plataforma. O produto é independente, mas pode ser integrado a sistemas externos:

- **Sistemas das Secretarias de Educação / MEC:** envio de dados acadêmicos, estatísticas e relatórios oficiais.

- **Ambientes Virtuais de Aprendizagem (AVA),** como Google Classroom ou Moodle, para complementar atividades pedagógicas online.

- **Sistemas financeiros/bancários:** emissão de boletos, controle de mensalidades e pagamentos.

- **Serviços de autenticação:** Single Sign-On (SSO), Google ou Microsoft, para facilitar o acesso de alunos e professores.

A arquitetura segue o modelo cliente-servidor: o cliente (front-end) é a interface web e mobile; o servidor (back-end) processa as regras de negócio, integra-se ao banco de dados e comunica-se com serviços externos. O banco de dados será relacional (PostgreSQL) e, em casos específicos, não relacional (NoSQL) para dados mais dinâmicos, como registros de atividades e comunicação instantânea.

## 4.2 Resumo das capacidades

| **Benefício para o cliente**                                                    | **Recursos de suporte**                                                                          |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Alunos e responsáveis acompanham em tempo real notas, frequência e comunicados. | Painel personalizado por usuário, notificações automáticas e integração com dispositivos móveis. |
| Professores têm maior agilidade no registro de notas, presenças e atividades.   | Interfaces intuitivas para avaliações, integração com planilhas e diário de classe digital.      |
| A secretaria reduz o retrabalho e centraliza documentos e dados escolares.      | Gestão automatizada de matrículas, emissão de boletins, relatórios e documentos oficiais.        |
| Gestores têm visão clara e estratégica do desempenho escolar e administrativo.  | Relatórios analíticos, dashboards com indicadores e exportação de dados.                         |
| A comunicação entre escola e famílias torna-se mais rápida e organizada.        | Mensageria interna, comunicados, mural digital e integração com e-mail/SMS.                      |
| Controle eficiente da parte financeira da instituição.                          | Módulo de cobranças, boletos, controle de inadimplência e integração com bancos.                 |
| Suporte técnico e pedagógico acessível e contínuo.                              | Base de conhecimento, tutoriais integrados e canal de suporte via chat/FAQ.                      |

## 4.3 Suposições e dependências

Caso alguma das condições abaixo seja alterada, será necessária a revisão deste documento.

- **Infraestrutura tecnológica:** a instituição dispõe de internet estável e equipamentos compatíveis (computadores, tablets e smartphones).

- **Navegadores e sistemas operacionais:** dependência dos principais navegadores (Chrome, Firefox, Edge) e sistemas operacionais amplamente utilizados.

- **Serviços de terceiros:** gateways de pagamento, e-mail e notificações push.

- **Capacitação dos usuários:** professores, alunos, gestores e demais usuários receberão treinamento básico.

- **Segurança e LGPD:** adesão às normas de proteção de dados e boas práticas de segurança, pela plataforma e pelas instituições.

- **Suporte técnico:** haverá equipe de suporte e manutenção preventiva.

- **Ambiente escolar:** a escola lançará notas, frequência e comunicados de forma consistente, garantindo a confiabilidade dos dados.

## 4.4 Custo e precificação

- **Modelo de precificação:** assinatura ajustada ao porte da instituição e à quantidade de alunos cadastrados.

- **Infraestrutura:** servidores em nuvem, com custo recorrente de operação.

- **Manutenção e suporte:** recursos para equipe de suporte e manutenção evolutiva.

- **Capacitação:** materiais de treinamento e suporte inicial para professores, gestores e equipe administrativa.

- **Integrações:** gateways de pagamento, e-mail e APIs de terceiros podem gerar custos de licenciamento e uso.

- **Restrições orçamentárias:** instituições menores podem ter limitações financeiras, o que exige precificação flexível e versões escalonadas.

## 4.5 Licenciamento e instalação

O licenciamento será baseado em uso autorizado por instituição, conforme o contrato de assinatura, com níveis de licença de acordo com o número de alunos e os recursos contratados. Todas as licenças estarão vinculadas a políticas de segurança que asseguram confidencialidade e integridade dos dados escolares, respeitando a LGPD.

A plataforma será disponibilizada preferencialmente em ambiente web, reduzindo a necessidade de instalação local. Poderá ser prevista a disponibilização de aplicativos móveis, com processos de publicação e atualização nas lojas oficiais (Google Play e App Store). Criptografia de senhas, autenticação de usuários e gerenciamento de sessões serão tratados como parte do esforço de desenvolvimento.

# 5\. Recursos do Produto

Esta seção lista os 31 requisitos identificados. Os campos “Origem” em que constava “0000” (sem referência real) foram substituídos por “—”. A prioridade foi padronizada em Alta, Média e Baixa.

## 5.1 Quadro-resumo dos requisitos

| **ID**  | **Recurso**                                         | **Tipo**      | **Prioridade** | **Solicitante**     |
|---------|-----------------------------------------------------|---------------|----------------|---------------------|
| REQ0001 | Nome de acesso (login) do usuário                   | Não funcional | Média          | Setor de TI         |
| REQ0002 | Senha de acesso dos usuários                        | Não funcional | Média          | Setor de TI         |
| REQ0003 | Boletim de notas dos alunos                         | Funcional     | Alta           | Coordenação         |
| REQ0004 | Agenda de atividades                                | Funcional     | Baixa          | Coordenação         |
| REQ0005 | Ocorrências (quebra das regras da escola)           | Funcional     | Baixa          | Coordenação         |
| REQ0006 | Informações de matrícula e dados do aluno           | Funcional     | Alta           | Secretaria          |
| REQ0007 | Grade de horários de professores e alunos           | Funcional     | Baixa          | Coordenação         |
| REQ0008 | Lista de alunos                                     | Funcional     | Alta           | Secretaria          |
| REQ0009 | Lista de funcionários                               | Funcional     | Média          | Recursos Humanos    |
| REQ0010 | Turmas e alunos de cada turma                       | Funcional     | Alta           | Secretaria          |
| REQ0011 | Quadro geral de avisos                              | Funcional     | Baixa          | Diretoria da Escola |
| REQ0012 | Emissão de relatórios                               | Funcional     | Alta           | Diretoria da Escola |
| REQ0013 | Emissão de certificados                             | Funcional     | Média          | Secretaria          |
| REQ0014 | Frequência dos alunos                               | Funcional     | Alta           | Coordenação         |
| REQ0015 | Plano de aula                                       | Funcional     | Média          | Coordenação         |
| REQ0016 | Backup                                              | Não funcional | Média          | Setor de TI         |
| REQ0017 | Validação de dados (RA, CPF, e-mail)                | Não funcional | Média          | Setor de TI         |
| REQ0018 | Criação de novo ano letivo                          | Funcional     | Média          | Secretaria          |
| REQ0019 | Configuração do novo calendário (apenas Secretaria) | Funcional     | Média          | Secretaria          |
| REQ0020 | Aviso de eventos escolares                          | Funcional     | Média          | Diretoria da Escola |
| REQ0021 | Efetuar matrícula                                   | Funcional     | Média          | Secretaria          |
| REQ0022 | Efetuar rematrícula                                 | Funcional     | Média          | Secretaria          |
| REQ0023 | Avaliações                                          | Funcional     | Média          | Coordenação         |
| REQ0024 | Solicitação de relatórios                           | Funcional     | Média          | Diretoria           |
| REQ0025 | Acesso simultâneo de usuários                       | Não funcional | Média          | Setor de TI         |
| REQ0026 | Disponibilidade 24 horas                            | Não funcional | Média          | Setor de TI         |
| REQ0027 | Tempo de resposta                                   | Não funcional | Média          | Setor de TI         |
| REQ0028 | Controle de acesso                                  | Não funcional | Alta           | Setor de TI         |
| REQ0029 | Histórico de alterações                             | Não funcional | Média          | Setor de TI         |
| REQ0030 | Suporte a diferentes resoluções de tela             | Não funcional | Média          | Setor de TI         |
| REQ0031 | Atalhos de teclado                                  | Não funcional | Baixa          | Usuários finais     |

## 5.2 Detalhamento dos requisitos

### REQ0001 – Nome de acesso (login) do usuário

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O login do usuário deverá ser um identificador único e inequívoco: e-mail cadastrado, RA (alunos) ou CPF (funcionários e responsáveis). O nome completo continuará sendo exibido no sistema, mas não será usado como credencial, para evitar conflitos entre homônimos.

### REQ0002 – Senha de acesso dos usuários

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** A senha deverá conter no mínimo oito caracteres, incluindo letras maiúsculas e minúsculas, números e caracteres especiais. As senhas deverão ser armazenadas com criptografia (hash com salt) e nunca em texto puro.

### REQ0003 – Boletim de notas dos alunos

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Alta           | Baixa             | Coordenação     | —          | Baixo            |

**Descrição:** A área do boletim apresentará as notas obtidas pelo aluno em provas e trabalhos. As notas poderão ser organizadas de forma bimestral, trimestral ou semestral, conforme definido pela instituição. Os registros serão separados por disciplina e o cálculo da média seguirá os critérios da instituição. (Prioridade elevada de Baixa para Alta, por coerência com a necessidade nº 6 da seção 3.7, de importância 5.)

### REQ0004 – Agenda de atividades

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Baixa          | Baixa             | Coordenação     | —          | Baixo            |

**Descrição:** O sistema deverá permitir o cadastro na agenda das atividades escolares, incluindo tarefas, projetos e avaliações. Os alunos terão acesso para visualizar as atividades.

### REQ0005 – Ocorrências (quebra das regras da escola)

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Baixa          | Baixa             | Coordenação     | —          | Baixo            |

**Descrição:** A área de ocorrências registrará quebras das regras estabelecidas pela escola, incluindo infrações disciplinares. Cada ocorrência deverá conter a data, a descrição do ocorrido e, se aplicável, as medidas adotadas pela instituição.

### REQ0006 – Informações de matrícula e dados do aluno

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Alta           | Alta              | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá armazenar e gerenciar as informações de matrícula dos alunos: dados pessoais (nome, data de nascimento, CPF, endereço, contato dos responsáveis), histórico acadêmico e status da matrícula. As informações deverão ser protegidas, garantindo integridade e confidencialidade, e apenas usuários autorizados poderão visualizá-las ou modificá-las, em conformidade com a LGPD.

### REQ0007 – Grade de horários de professores e alunos

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Baixa          | Baixa             | Coordenação     | —          | Baixo            |

**Descrição:** A área de Horários apresentará a grade de professores e alunos, incluindo períodos das aulas, disciplinas e docentes. A organização poderá seguir o formato diário ou semanal, conforme a instituição.

### REQ0008 – Lista de alunos

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Alta           | Alta              | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá disponibilizar a lista de alunos matriculados, com consulta por nome, turma, série e status da matrícula, exibindo nome completo, número de matrícula e contato dos responsáveis. Somente usuários autorizados poderão visualizar e gerenciar esses dados.

### REQ0009 – Lista de funcionários

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante**  | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|------------------|------------|------------------|
| Funcional | Média          | Alta              | Recursos Humanos | —          | Baixo            |

**Descrição:** O sistema deverá permitir cadastro, consulta e edição de funcionários, apresentando nome completo, cargo/função, setor, e-mail, telefone e situação (ativo/inativo), com busca por filtros (nome, cargo, setor).

### REQ0010 – Turmas e alunos de cada turma

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Alta           | Alta              | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá permitir organizar e visualizar os alunos por turma, exibindo a lista de matriculados em cada uma, com busca por série, turno e ano letivo. Apenas usuários autorizados poderão visualizar e atualizar essas informações.

### REQ0011 – Quadro geral de avisos

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante**     | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|---------------------|------------|------------------|
| Funcional | Baixa          | Baixa             | Diretoria da Escola | —          | Baixo            |

**Descrição:** O Quadro Geral de Avisos divulgará comunicados da instituição (avisos administrativos, eventos, prazos, mudanças na grade, orientações gerais). Os avisos poderão ser categorizados por nível de importância (normal, importante, urgente) e direcionados a públicos específicos.

### REQ0012 – Emissão de relatórios

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante**     | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|---------------------|------------|------------------|
| Funcional | Alta           | Alta              | Diretoria da Escola | —          | Baixo            |

**Descrição:** O sistema deverá permitir a geração e exportação de relatórios acadêmicos e administrativos (listas de alunos, frequência, notas, matrículas e desempenho escolar) em PDF e Excel, acessíveis apenas a usuários autorizados. (Tipo corrigido de Não funcional para Funcional.)

### REQ0013 – Emissão de certificados

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Média             | Secretaria      | —          | Baixo            |

**Descrição:** A área de Emissão de Certificados permitirá gerar e disponibilizar certificados oficiais (conclusão de cursos, participação em eventos, atividades extracurriculares, premiações). Os certificados poderão ser acessados por alunos e responsáveis conforme as permissões da instituição.

### REQ0014 – Frequência dos alunos

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Alta           | Baixa             | Coordenação     | —          | Baixo            |

**Descrição:** A área de Frequência permitirá registrar e acompanhar a presença dos estudantes, de forma diária e por disciplina, registrando presenças, faltas e justificativas. A justificativa será aceita apenas nos casos previstos pelas normas da instituição (atestado médico, eventos oficiais, falecimento de familiar próximo e outras situações comprovadas). As informações ficarão disponíveis a alunos, responsáveis e equipe pedagógica conforme as permissões, e o sistema poderá gerar relatórios periódicos e alertas de faltas. (Prioridade elevada de Baixa para Alta, por coerência com a necessidade nº 7 da seção 3.7, de importância 5.)

### REQ0015 – Plano de aula

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Média             | Coordenação     | —          | Baixo            |

**Descrição:** O sistema deverá permitir que professores criem, editem e gerenciem planos de aula (conteúdos, objetivos, metodologias e avaliações), organizados por disciplina, turma e período letivo, com opção de compartilhamento entre docentes e coordenação pedagógica. (Solicitante corrigido de Secretaria para Coordenação.)

### REQ0016 – Backup

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá realizar backups automáticos e programados dos dados (registros acadêmicos, históricos e administrativos), sem afetar o desempenho, armazenados com segurança e controle de integridade, permitindo restauração rápida em caso de falha ou perda de dados.

### REQ0017 – Validação de dados (RA, CPF, e-mail)

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá validar os dados inseridos, com foco no Registro Acadêmico (RA), garantindo que cada RA seja único e verificando o formato de CPF e e-mail. Em caso de dados duplicados ou inválidos, o usuário deverá ser alertado e solicitado a corrigir antes de prosseguir.

### REQ0018 – Criação de novo ano letivo

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Baixa             | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá permitir a criação automatizada de um novo ano letivo, preservando as informações dos anos anteriores (notas, frequência e matrículas) e transferindo os alunos para as turmas correspondentes, com configuração de novos períodos sem perda de histórico. (Tipo corrigido para Funcional; solicitante corrigido para Secretaria.)

### REQ0019 – Configuração do novo calendário (apenas Secretaria)

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Baixa             | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá possibilitar à Secretaria configurar o calendário letivo (início e término das aulas, feriados, recessos e eventos). A configuração será restrita à Secretaria e poderá ser ajustada ao longo do ano. (Tipo corrigido para Funcional.)

### REQ0020 – Aviso de eventos escolares

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante**     | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|---------------------|------------|------------------|
| Funcional | Média          | Baixa             | Diretoria da Escola | 0011       | Baixo            |

**Descrição:** O sistema deverá permitir criar e enviar avisos sobre eventos escolares (reuniões de pais, festas, atividades extracurriculares), direcionados a públicos específicos (alunos, pais, professores e funcionários), visíveis na plataforma e registrados com data, descrição e público-alvo. (Tipo corrigido para Funcional.)

### REQ0021 – Efetuar matrícula

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Baixa             | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá permitir a matrícula de novos alunos, registrando dados pessoais, contato dos responsáveis e informações do curso. Deverá gerar automaticamente o número de matrícula e enviar confirmação por e-mail ou notificação, conforme a preferência da instituição, de forma simples e sem inconsistências.

### REQ0022 – Efetuar rematrícula

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Baixa             | Secretaria      | —          | Baixo            |

**Descrição:** O sistema deverá permitir a rematrícula automatizada, sem novo cadastro completo, incluindo atualização de dados do aluno e responsáveis, escolha de disciplinas (quando aplicável) e confirmação da renovação do vínculo, com notificações sobre o período e o status do processo.

### REQ0023 – Avaliações

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Baixa             | Coordenação     | 0004       | Baixo            |

**Descrição:** O sistema deverá permitir que professores cadastrem, editem e acompanhem provas, registrando notas, critérios de correção e feedbacks, associadas a disciplinas e turmas. Alunos e responsáveis poderão ver notas e status conforme as permissões.

### REQ0024 – Solicitação de relatórios

| **Tipo**  | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|-----------|----------------|-------------------|-----------------|------------|------------------|
| Funcional | Média          | Baixa             | Diretoria       | 0012       | Baixo            |

**Descrição:** Complementa o REQ0012: permite que a Diretoria e a Secretaria solicitem relatórios sob demanda (listas de presença, notas, matrículas, desempenho), gerados em PDF ou Excel e disponíveis conforme as permissões. A emissão em si segue o REQ0012; este requisito trata do fluxo de solicitação e acompanhamento.

### REQ0025 – Acesso simultâneo de usuários

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá suportar múltiplos usuários acessando a plataforma simultaneamente, cada um com credenciais individuais e permissões apropriadas ao seu perfil, sem conflitos ou perda de integridade dos dados e mantendo a mesma experiência independentemente da quantidade de acessos. É vedado o compartilhamento de um mesmo login entre pessoas. (Corrigido: a versão original previa vários usuários com o mesmo login, o que contradizia o REQ0028 e a segurança do sistema.)

### REQ0026 – Disponibilidade 24 horas

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá estar acessível 24 horas por dia, com disponibilidade mínima de 99%, com redundância e monitoramento para detectar e corrigir falhas rapidamente.

### REQ0027 – Tempo de resposta

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá garantir tempos de resposta rápidos, inclusive em períodos de pico: páginas carregadas em até 3 segundos e relatórios gerados quase instantaneamente (metas da seção 7).

### REQ0028 – Controle de acesso

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Alta           | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá possuir controle de acesso por perfil, garantindo que dados sensíveis e administrativos sejam acessados apenas por pessoas autorizadas, com gestão centralizada das permissões pelos administradores. (Prioridade elevada de Média para Alta, pois sustenta a conformidade com a LGPD.)

### REQ0029 – Histórico de alterações

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá manter histórico detalhado das alterações em informações acadêmicas e administrativas (matrículas, notas, dados pessoais), acessível apenas a usuários autorizados, permitindo auditoria e recuperação de versões anteriores.

### REQ0030 – Suporte a diferentes resoluções de tela

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Média          | Baixa             | Setor de TI     | —          | Baixo            |

**Descrição:** O sistema deverá ser responsivo, ajustando-se automaticamente a dispositivos móveis, tablets e computadores, com navegação e interação consistentes em todas as plataformas.

### REQ0031 – Atalhos de teclado

| **Tipo**      | **Prioridade** | **Imutabilidade** | **Solicitante** | **Origem** | **Impacto arq.** |
|---------------|----------------|-------------------|-----------------|------------|------------------|
| Não funcional | Baixa          | Baixa             | Usuários finais | —          | Baixo            |

**Descrição:** O sistema deverá fornecer atalhos de teclado configuráveis e documentados (salvar, acessar menus, navegar entre telas) para permitir uma navegação ágil sem depender constantemente do mouse ou do toque.

## 5.3 Diagramas

### Diagrama de casos de uso

<img src="imagens/media/496708ec66b52e234a0f091133b02a82c11de433.png" title="Figura 1 – Diagrama de casos de uso" style="width:6.25in;height:2in" alt="Figura 1 – Diagrama de casos de uso" />

*Figura 1 – Diagrama de casos de uso*

### Diagrama de classes

<img src="imagens/media/0ce03d7cf9024b8b4981f8ac9c3f6d039dd8935b.png" title="Figura 2 – Diagrama de classes" style="width:6.45833in;height:6.45833in" alt="Figura 2 – Diagrama de classes" />

*Figura 2 – Diagrama de classes*

### Diagrama de objetos

*Os dados exibidos são fictícios; CPF, PIS, senha, data de nascimento e endereço foram substituídos por valores genéricos.*

<img src="imagens/media/6fb21cd0732cab43ae73d1c4f4bd84dbfef854f1.png" title="Figura 3 – Diagrama de objetos" style="width:6.45833in;height:6.45833in" alt="Figura 3 – Diagrama de objetos" />

*Figura 3 – Diagrama de objetos*

### Diagrama de componentes

<img src="imagens/media/e4f1209f9e7617451dfa411bd755c7c5111b889b.png" title="Figura 4 – Diagrama de componentes do sistema" style="width:5.08333in;height:3.07292in" alt="Figura 4 – Diagrama de componentes do sistema" />

*Figura 4 – Diagrama de componentes do sistema*

### Diagrama de colaboração e estrutura composta

<img src="imagens/media/6a62620d54ee508fb92d4a050d8c9c616044f556.png" title="Figura 5 – Colaboração (emissão de relatório) e estrutura composta (chamada)" style="width:6.25in;height:2.04167in" alt="Figura 5 – Colaboração (emissão de relatório) e estrutura composta (chamada)" />

*Figura 5 – Colaboração (emissão de relatório) e estrutura composta (chamada)*

### Máquinas de estado

<img src="imagens/media/5e8f8dcc2aee67282e5a91e3c76e10565e683d44.png" title="Figura 6 – Máquina de estados do processo de matrícula" style="width:6.25in;height:2.04167in" alt="Figura 6 – Máquina de estados do processo de matrícula" />

*Figura 6 – Máquina de estados do processo de matrícula*

<img src="imagens/media/36e350462f5cb3d127f6029ab1161fbe565c7c70.png" title="Figura 7 – Máquina de estados da criação de avaliação e inserção de notas" style="width:5.35417in;height:1.53125in" alt="Figura 7 – Máquina de estados da criação de avaliação e inserção de notas" />

*Figura 7 – Máquina de estados da criação de avaliação e inserção de notas*

### Diagramas de atividades

<img src="imagens/media/3c8af489df6c091eaf5a8d1c86bdfcac4d08133c.png" title="Figura 8 – Atividades: chamada" style="width:3.14583in;height:2.72917in" alt="Figura 8 – Atividades: chamada" />

*Figura 8 – Atividades: chamada*

<img src="imagens/media/67826b8fdec62605308b6d594dcc2d88babadda4.png" title="Figura 9 – Atividades: registro de notas dos alunos" style="width:3.0625in;height:3.04167in" alt="Figura 9 – Atividades: registro de notas dos alunos" />

*Figura 9 – Atividades: registro de notas dos alunos*

### Diagramas de sequência

<img src="imagens/media/3d3c30ef4e6cd5a4af35f7c357766833e6d9fcd6.png" title="Figura 10 – Sequência: consulta de notas do aluno" style="width:4.54167in;height:1.92708in" alt="Figura 10 – Sequência: consulta de notas do aluno" />

*Figura 10 – Sequência: consulta de notas do aluno*

<img src="imagens/media/20f70c314dc64ba4cb348e469b2c1746b11e65ab.png" title="Figura 11 – Sequência: chamada" style="width:4.67708in;height:2.39583in" alt="Figura 11 – Sequência: chamada" />

*Figura 11 – Sequência: chamada*

## 5.4 Protótipos de tela

### Primeira versão (desktop)

<img src="imagens/media/a20516b6f5da857ad00d2dd489bcc207883f8cf6.png" title="Figura 12 – Ocorrências" style="width:4.47917in;height:2.23958in" alt="Figura 12 – Ocorrências" />

*Figura 12 – Ocorrências*

<img src="imagens/media/3aceb5a9ce8d901c1c7a5cec511058aeebc7681b.png" title="Figura 13 – Atividades postadas (detalhe)" style="width:4.47917in;height:2.25in" alt="Figura 13 – Atividades postadas (detalhe)" />

*Figura 13 – Atividades postadas (detalhe)*

<img src="imagens/media/bd0e160149cc9dc425f122b39e6531306a43b5c3.png" title="Figura 14 – Atividades postadas" style="width:4.47917in;height:2.23958in" alt="Figura 14 – Atividades postadas" />

*Figura 14 – Atividades postadas*

<img src="imagens/media/cc17509369a7daa5a304aa8917e3c550517689f2.png" title="Figura 15 – Desempenho acadêmico" style="width:4.47917in;height:2.27083in" alt="Figura 15 – Desempenho acadêmico" />

*Figura 15 – Desempenho acadêmico*

<img src="imagens/media/d317e97bc309cc44889857adcaefea2263cd6ec7.png" title="Figura 16 – Calendário" style="width:4.47917in;height:2.23958in" alt="Figura 16 – Calendário" />

*Figura 16 – Calendário*

<img src="imagens/media/2203b311744f66026e0573711dac744adcf78926.png" title="Figura 17 – Calendário (frequência do dia)" style="width:4.47917in;height:2.23958in" alt="Figura 17 – Calendário (frequência do dia)" />

*Figura 17 – Calendário (frequência do dia)*

### Primeira versão (mobile)

<img src="imagens/media/bd1acf0c9a762e2ceac08e2b92bb4b10d82b668a.png" title="Figura 18 – Calendário" style="width:2.07292in;height:3.5in" alt="Figura 18 – Calendário" />

*Figura 18 – Calendário*

<img src="imagens/media/47b3af3c21d4a82e62da207e74a35bac197f3b2a.png" title="Figura 19 – Atividades" style="width:2.08333in;height:3.46875in" alt="Figura 19 – Atividades" />

*Figura 19 – Atividades*

<img src="imagens/media/1b1d33915629bf774e96c52ca5b7f7b6b6b0500c.png" title="Figura 20 – Desempenho acadêmico" style="width:2.08333in;height:3.52083in" alt="Figura 20 – Desempenho acadêmico" />

*Figura 20 – Desempenho acadêmico*

<img src="imagens/media/d9a047067a742c644343daee5386f50204ecacfa.png" title="Figura 21 – Ocorrências" style="width:2.08333in;height:3.5in" alt="Figura 21 – Ocorrências" />

*Figura 21 – Ocorrências*

### Telas atualizadas

<img src="imagens/media/b3db1334b2653da049f0ff228be291a694907ae4.png" title="Figura 22 – Faltas (sem registro)" style="width:4.47917in;height:2.34375in" alt="Figura 22 – Faltas (sem registro)" />

*Figura 22 – Faltas (sem registro)*

<img src="imagens/media/c4ce8aaf2a44111ff01a42e6adf08442d1693a06.png" title="Figura 23 – Faltas (dia com falta)" style="width:4.47917in;height:2.33333in" alt="Figura 23 – Faltas (dia com falta)" />

*Figura 23 – Faltas (dia com falta)*

<img src="imagens/media/f1d6370292270015cae6f9f003368a8185b15bb0.png" title="Figura 24 – Quadro de avisos" style="width:4.47917in;height:2.375in" alt="Figura 24 – Quadro de avisos" />

*Figura 24 – Quadro de avisos*

<img src="imagens/media/5b3a4530665e01b392f2430076e2de5608ef5b5e.png" title="Figura 25 – Horário de hoje" style="width:4.47917in;height:2.34375in" alt="Figura 25 – Horário de hoje" />

*Figura 25 – Horário de hoje*

<img src="imagens/media/2ecaaf4d0170de7107d29676d56b03f9617ce1e4.png" title="Figura 26 – Notas" style="width:4.47917in;height:2.35417in" alt="Figura 26 – Notas" />

*Figura 26 – Notas*

# 6\. Restrições

O desenvolvimento da plataforma está sujeito a restrições que precisam ser observadas para garantir sua viabilidade técnica, legal e operacional:

- **Restrições de design:** interface responsiva e acessível em computadores, tablets e smartphones, respeitando diretrizes de usabilidade e acessibilidade, com padrão consistente entre todos os módulos.

- **Restrições tecnológicas:** arquitetura web compatível com navegadores modernos e sistemas operacionais amplamente utilizados; operação em nuvem, assegurando disponibilidade e escalabilidade; compatibilidade com bancos relacionais e não relacionais.

- **Restrições operacionais:** disponibilidade mínima de 99%, suporte a acessos simultâneos em períodos de pico (fechamento de notas e matrículas) e tempo de resposta adequado em operações críticas.

- **Restrições regulamentares:** atendimento à LGPD no armazenamento, tratamento e compartilhamento de dados pessoais de alunos, responsáveis, professores e funcionários, além de normas educacionais e de órgãos oficiais. Por envolver dados de crianças e adolescentes, deve-se observar também o tratamento específico previsto na LGPD e no ECA.

- **Restrições de dependência:** acesso constante à internet para funcionalidades em tempo real e integrações com terceiros (gateways de pagamento, e-mail, notificações móveis), que podem impactar a disponibilidade em caso de falhas externas.

# 7\. Faixas de Qualidade

O projeto Triledu visa não apenas entregar um sistema funcional, mas garantir que sua operação atenda a altos padrões de qualidade:

- **Usabilidade:** interface intuitiva e de fácil acesso para professores, alunos e responsáveis em qualquer dispositivo.

- **Desempenho:** carregamento de páginas em até 3 segundos e geração de relatórios quase instantânea.

- **Robustez:** uptime mínimo de 99%, com mecanismos de backup e recuperação que garantam persistência e integridade dos dados.

- **Segurança:** autenticação rigorosa e criptografia, em conformidade com a LGPD.

- **Escalabilidade:** crescimento do número de usuários sem comprometer a estabilidade ou a eficiência.

# 8\. Precedência e Prioridade

A tabela classifica os recursos conforme o benefício para o usuário final (ver seção 11.2) e sugere uma ordem de implementação. Trata-se de uma proposta inicial, a ser validada com a Direção Escolar e a Profissional da Educação.

| **Fase**                               | **Recursos**                                                                                                                                                                            | **Justificativa**                                                                            |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| 1 – Crítico (base do sistema)          | REQ0001, 0002, 0028 (login e controle de acesso); REQ0006, 0008, 0009, 0010 (cadastros); REQ0017 (validação de dados); REQ0021, 0022 (matrícula e rematrícula)                          | Sem esses recursos o sistema não opera; os demais módulos dependem deles.                    |
| 2 – Crítico (núcleo pedagógico)        | REQ0003, 0023 (notas e avaliações); REQ0014 (frequência); REQ0012, 0024 (relatórios)                                                                                                    | Atendem às necessidades de importância 5 da seção 3.7.                                       |
| 3 – Importante                         | REQ0011, 0020 (avisos e eventos); REQ0004 (agenda); REQ0007 (horários); REQ0015 (plano de aula); REQ0018, 0019 (ano letivo e calendário); REQ0013 (certificados); REQ0005 (ocorrências) | Melhoram a eficácia e a comunicação, mas o sistema funciona sem eles em uma primeira versão. |
| Transversal (acompanha todas as fases) | REQ0016 (backup), 0025, 0026, 0027, 0029, 0030                                                                                                                                          | Requisitos não funcionais que devem ser considerados desde a arquitetura.                    |
| 4 – Útil                               | REQ0031 (atalhos de teclado)                                                                                                                                                            | Uso menos frequente; pode ficar para uma versão posterior.                                   |

# 9\. Outros Requisitos do Produto

## 9.1 Padrões aplicáveis

- Jurídicos e regulamentares: LGPD (Lei nº 13.709/2018), ECA (Lei nº 8.069/1990) e normas do MEC para envio de dados educacionais.

- Comunicação: HTTPS/TLS para todo o tráfego; protocolos TCP/IP.

- Acessibilidade: recomendações WCAG 2.1 (nível AA).

- Qualidade e segurança: boas práticas inspiradas nas famílias ISO/IEC 25010 (qualidade de produto) e ISO/IEC 27001 (segurança da informação), como referência — sem pretensão de certificação nesta fase.

## 9.2 Requisitos do sistema

- Acesso por navegadores modernos (Google Chrome, Mozilla Firefox e Microsoft Edge, em versões atualizadas) em Windows, Linux, macOS, Android e iOS.

- Servidor em nuvem com banco de dados PostgreSQL e, quando necessário, NoSQL.

- Não há exigência de software adicional no cliente; periféricos (impressora, leitor de PDF) apenas para emissão de documentos.

## 9.3 Requisitos de desempenho

- Carregamento de páginas em até 3 segundos em condições normais.

- Disponibilidade mínima de 99%.

- Suporte a picos de acesso simultâneo (fechamento de notas e período de matrículas), com escalabilidade e balanceamento de carga.

- Geração de relatórios quase instantânea.

## 9.4 Requisitos ambientais

- Uso em escolas urbanas e suburbanas com internet banda larga ou móvel; previsão de modo offline/leve para instabilidades de conexão.

- Tratamento de erros com mensagens claras ao usuário e recuperação por backups programados.

- Manutenção preventiva e evolutiva realizada pela equipe técnica, preferencialmente fora dos horários de pico escolar.

# 10\. Requisitos de Documentação

## 10.1 Notas sobre a liberação (Leia-me)

Cada versão acompanhará notas de liberação com novidades, problemas de compatibilidade com versões anteriores, instruções de atualização e problemas conhecidos.

## 10.2 Ajuda on-line

A plataforma contará com base de conhecimento, tutoriais integrados e FAQ, conforme previsto na seção 4.2, com conteúdo adequado a cada perfil de usuário.

## 10.3 Guias de instalação

Documento com instruções de implantação, configuração do ambiente em nuvem e atualização, voltado à equipe técnica.

## 10.4 Rótulo e embalagem

Padronização visual da marca Triledu (logotipo, ícones, cores e avisos de direitos autorais) em telas de login, menus, mensagens do sistema e documentos emitidos.

# 11\. Apêndice 1 – Atributos do Recurso

## 11.1 Status

| **Status**  | **Descrição**                                                         |
|-------------|-----------------------------------------------------------------------|
| Proposto    | Recurso em discussão, ainda não revisado e aceito pelo canal oficial. |
| Aprovado    | Recurso considerado útil e factível, aprovado para implementação.     |
| Incorporado | Recurso incorporado à linha de base do produto.                       |

*Situação atual: todos os 31 requisitos encontram-se no status Proposto.*

## 11.2 Benefício

| **Prioridade** | **Descrição**                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Crítico        | Recursos essenciais; sua ausência faz o sistema não atender às necessidades do cliente.                          |
| Importante     | Recursos importantes para a eficácia do sistema; omiti-los pode afetar a satisfação, mas não atrasa a liberação. |
| Útil           | Recursos usados com menos frequência ou com alternativas razoáveis; sem impacto significativo se omitidos.       |

## 11.3 Esforço

Estimado pela equipe de desenvolvimento para cada recurso (tempo, código ou funções), para calibrar a complexidade e gerenciar o escopo. A estimativa será feita quando a stack tecnológica for definida.

## 11.4 Risco

Classificado em alto, médio ou baixo, conforme a probabilidade de estouro de custos, atrasos ou cancelamento, avaliada pela incerteza da estimativa de cronograma.

## 11.5 Estabilidade

Indica a probabilidade de o recurso mudar ou de o entendimento da equipe sobre ele mudar, ajudando a priorizar o desenvolvimento e a identificar itens que exigem nova descoberta.

## 11.6 Liberação de destino

Versão do produto que incluirá o recurso. Somente recursos com status Incorporado e liberação de destino definida serão implementados.

## 11.7 Designado para

Equipe responsável pelo detalhamento e implementação do recurso, conforme os papéis descritos na seção 3.5.

## 11.8 Motivo

Origem do recurso solicitado, registrada no campo “Solicitante” de cada requisito (seção 5.2).

# 12\. Apêndice 2 – Cronograma

Proposta de cronograma por ciclo quinzenal, conforme a cadência atual do projeto (seção 3.4). As atividades de desenvolvimento ainda não foram iniciadas; as datas e a quantidade de ciclos devem ser ajustadas pela equipe.

| **Atividade**                                               | **Ciclo 1** | **Ciclo 2** | **Ciclo 3** | **Ciclo 4** | **Ciclo 5** | **Ciclo 6+** |
|-------------------------------------------------------------|-------------|-------------|-------------|-------------|-------------|--------------|
| Levantamento de requisitos e documento de visão (concluído) | X           | X           |             |             |             |              |
| Modelagem UML e protótipos de tela (concluído)              |             | X           | X           |             |             |              |
| Definição da stack e da arquitetura                         |             |             | X           | X           |             |              |
| Modelagem e criação do banco de dados                       |             |             |             | X           | X           |              |
| Desenvolvimento do back-end (API REST)                      |             |             |             | X           | X           | X            |
| Desenvolvimento do front-end                                |             |             |             |             | X           | X            |
| Testes de usabilidade com professores e responsáveis        |             |             |             |             |             | X            |
| Documentação de uso e entrega                               |             |             |             |             |             | X            |

# Apêndice 3 – Registro de revisão do documento

Alterações feitas em relação à versão de 06/06/2025:

- REQ0001: o login deixa de ser o nome completo (risco de homônimos) e passa a ser e-mail, RA ou CPF.

- REQ0002: incluída a exigência de armazenamento de senhas com hash e salt.

- REQ0012, 0018, 0019 e 0020: tipo corrigido para Funcional.

- REQ0025: removida a previsão de vários usuários com o mesmo login, que contradizia o REQ0028; passa a exigir credenciais individuais.

- REQ0003, 0014 e 0028: prioridade elevada para coerência com a seção 3.7 e com a LGPD.

- REQ0015 e 0018: solicitante ajustado (Coordenação e Secretaria, respectivamente).

- REQ0024: esclarecida a relação com o REQ0012 (emissão x solicitação).

- Prioridade e imutabilidade padronizadas em Alta/Média/Baixa; origem “0000” substituída por “—”.

- Seção 3.2 e 3.3 preenchidas (continham o texto do modelo); seção 3.5 e 3.6 condensadas em tabelas.

- Representante de Alunos e Responsáveis alterado de “Secretaria Escolar” para “Direção Escolar / Mantenedora”.

- Seções 8, 9, 10, 11 e 12 preenchidas (continham o texto do modelo IBM). O conteúdo das seções 8, 9 e 12 é uma proposta e deve ser validado pelo grupo.

- Removidos o texto introdutório do modelo IBM e trechos soltos do modelo (ex.: “requisitos de instalação também podem afetar a codificação...”).

- Diagrama de objetos: CPF, PIS, senha, data de nascimento e endereço substituídos por dados genéricos.

- Incluída observação para confirmar a fonte e o ano dos dados do INEP (seção 3.1).

- Incluída menção ao ECA nas restrições regulamentares e capa com o status “software ainda não desenvolvido”.
