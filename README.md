# Triledu – Plataforma de Gestão Escolar

> **Status:** fase de documentação e prototipação. **O software ainda não foi desenvolvido.**
> Este repositório contém apenas o Documento de Visão e os artefatos de análise.

Projeto acadêmico do curso de **Bacharelado em Engenharia de Software (4º período)** do **UGV – Centro Universitário**, União da Vitória – PR.

## 📄 Documento de Visão

- **[Ler o Documento de Visão (Markdown, abre direto no GitHub)](docs/documento-de-visao.md)**
- [Baixar em PDF](docs/Documento_de_Visao_Triledu.pdf) · [Baixar em Word (.docx)](docs/Documento_de_Visao_Triledu.docx)

## Sobre o projeto

O Triledu é uma proposta de plataforma web responsiva que integra, em um único ambiente, os processos administrativos, pedagógicos e de comunicação de instituições de ensino, reduzindo a burocracia e facilitando a interação entre secretaria, professores, alunos, responsáveis e gestores.

## Problemas que se propõe a resolver

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
- Plano de aula e registro de ocorrências
- Backup, histórico de alterações e validação de dados (RA, CPF)

## Perfis de usuário

Professores · Alunos · Responsáveis · Secretaria · Gestores · Equipe técnica · Equipe de suporte

## Arquitetura planejada

- **Modelo:** cliente-servidor, aplicação web responsiva
- **Back-end:** API REST com regras de negócio
- **Banco de dados:** PostgreSQL (relacional), com NoSQL em casos específicos
- **Integrações previstas:** e-mail/push, API do MEC, AVAs (Google Classroom/Moodle), gateways de pagamento

## Metas de qualidade

- Disponibilidade mínima de 99%
- Carregamento de páginas em até 3 segundos
- Conformidade com a LGPD
- Escalabilidade para redes de ensino

## Diagramas

![Diagrama de casos de uso](docs/imagens/)

Os demais diagramas e os protótipos de tela estão na seção 5 do [Documento de Visão](docs/documento-de-visao.md).

## Equipe

Ana Vitória Basniak · Felipe Bernardino Silva · Gabriel Henrique Libmann · Igor Andriel Hetman · Luana Gabrielly Pszymus · Natali Lascoski · Rafael Roiek Correa

## Próximos passos

- [ ] Definir a stack tecnológica

## Licença

Veja o arquivo [LICENSE](LICENSE).
