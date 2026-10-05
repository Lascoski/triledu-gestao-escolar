# Triledu – Plataforma de Gestão Escolar

> 📄 **Status:** Documentação e prototipação. **O software não foi desenvolvido.**
> Este repositório contém apenas o Documento de Visão e artefatos de análise.

Projeto acadêmico do curso de **Bacharelado em Engenharia de Software (4º período)**

## Sobre o projeto

O Triledu é uma proposta de plataforma web responsiva para integrar, em um único
ambiente, os processos administrativos, pedagógicos e de comunicação de instituições
de ensino. A ideia é reduzir a burocracia e facilitar a interação entre secretaria,
professores, alunos, responsáveis e gestores.

## Problema que se propõe a resolver

- Sistemas instáveis e com interfaces pouco intuitivas
- Suporte técnico lento
- Falta de acesso adequado por dispositivos móveis
- Dificuldade em localizar documentos e registros acadêmicos
- Comunicação falha entre escola e famílias

## Funcionalidades previstas

- Login com controle de acesso por perfil
- Boletim de notas e avaliações
- Registro de frequência (chamada)
- Agenda de atividades e calendário letivo
- Matrícula e rematrícula
- Quadro de avisos e comunicados
- Emissão de relatórios (PDF/Excel) e certificados
- Plano de aula
- Registro de ocorrências
- Backup, histórico de alterações e validação de dados (RA, CPF)

## Perfis de usuário

Professores · Alunos · Responsáveis · Secretaria · Gestores · Equipe técnica · Equipe de suporte

## Arquitetura planejada

- **Modelo:** cliente-servidor, aplicação web responsiva
- **Front-end:** painéis por perfil (web/mobile)
- **Back-end:** API REST com regras de negócio
- **Banco de dados:** PostgreSQL (relacional), com NoSQL em casos específicos
- **Integrações previstas:** e-mail/push, API do MEC, AVAs (Google Classroom/Moodle), gateways de pagamento

## Requisitos de qualidade (metas)
- Disponibilidade mínima de 99%
- Carregamento de páginas em até 3 segundos
- Conformidade com a LGPD
- Escalabilidade para redes de ensino

## Conteúdo do repositório

| Pasta | Descrição |
|---|---|
| [`Documento_de_Visao_Triledu_c.docx`](docs/documento-de-visao.pdf) | Documento de Visão completo |
| [`docs/diagramas/`](docs/diagramas) | Casos de uso, classes, objetos, componentes, estados, atividades e sequência |
| [`prototipos/`](prototipos) | Telas prototipadas (versões 1 e 2) |

## Diagramas

![Diagrama de casos de uso](docs/diagramas/casos-de-uso.png)

## Protótipos de tela

![Tela de faltas](prototipos/telas-v2/faltas.png)

## Equipe

- Ana B, Felipe B, Luana P, Natali Lascoski, Rafael R

## Próximos passos

- [ ] Finalizar seções pendentes do Documento de Visão (cronograma, precedência e prioridade)
- [ ] Definir stack tecnológica

## Licença

Documentação distribuída sob a licença [MIT/CC BY 4.0].
