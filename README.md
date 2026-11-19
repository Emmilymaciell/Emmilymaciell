# Emmily Maciel — Engenharia civil · Automação documental · IA aplicada

[Português](#pt) · [English](#en)

<a id="pt"></a>
## Português

Atuo em engenharia civil, num programa de infraestrutura rodoviária, e construo as ferramentas que tiram o trabalho
documental repetitivo das mãos da equipe: relatórios gerados a partir das fontes, acervos no SharePoint
inventariados e pesquisáveis, dashboards com a origem de cada número. Os repositórios abaixo são cópias sanitizadas
desses sistemas, com dados fictícios e testes que rodam sem acesso ao dado real.

### Em que trabalho

- **Automação documental**: relatórios Word/PDF montados do zero a partir de planilhas e listas oficiais, com validação antes da entrega.
- **Sistemas documentais e SharePoint**: inventário, deduplicação e migração pelo Microsoft Graph, em modo somente leitura sempre que possível.
- **IA aplicada e agentes**: Claude Code e Codex como ferramentas de construção, com uma plataforma própria para governar projetos feitos com agentes.
- **Dashboards e dados**: Python, FastAPI, DuckDB, React; cada número exibido carrega a sua proveniência.
- **Engenharia**: BIM 4D, caminho crítico, coordenadas UTM, remessa e controle de documentos de projeto.

### Projetos em destaque

| Projeto | Problema → solução | Evidência | Tecnologias | Estado |
|---|---|---|---|---|
| [ai-project-os](https://github.com/Emmilymaciell/ai-project-os) | Projetos feitos com IA guardam o estado na conversa → plataforma que cria, versiona, verifica e protege cada projeto, com o repositório como fonte de verdade | 375 testes `unittest` do motor OK (19/11/2026); decisões em ADRs | Claude Code, Python (stdlib), PowerShell, Git hooks | em uso |
| [infra-4d-intelligence](https://github.com/Emmilymaciell/infra-4d-intelligence) | A previsão de término de obra linear vem de quem executa → recálculo independente pela produtividade medida, com motor CPM, Monte Carlo e visualizador 3D/4D | 2236 testes pytest passando, 6 pulados por exigirem navegador (19/11/2026); dados sintéticos | Python, FastAPI, IfcOpenShell, three.js | demonstração local |
| [cerebro-documental](https://github.com/Emmilymaciell/cerebro-documental) | Acervo de engenharia no SharePoint sem inventário nem busca → pipeline determinístico que inventaria, deduplica, extrai texto e indexa com citação de página | 17 suítes, 1726 PASS / 0 FAIL (19/11/2026); demo offline | Python, SQLite FTS5, Microsoft Graph | código pronto; massificação pendente |
| [relatorio-tecnico-automatizado](https://github.com/Emmilymaciell/relatorio-tecnico-automatizado) | Relatório técnico mensal feito copiando o mês anterior → modelo obtido por engenharia reversa e gerador que monta o documento do zero, comparado ao PDF publicado | 1068 passed (19/11/2026) | Python, python-docx, PyMuPDF, YAML | em uso |
| [dashboard-juridico](https://github.com/Emmilymaciell/dashboard-juridico) | Acervo jurídico só consultável contando linhas de planilha → ingestão somente leitura, modelo analítico com proveniência, API e dashboard | 149 testes Python + 120 de frontend (19/11/2026) | FastAPI, DuckDB, React, ECharts | em uso |
| [organizacao-sharepoint](https://github.com/Emmilymaciell/organizacao-sharepoint) | Biblioteca SharePoint acima da cota → inventário pela nuvem sem baixar arquivos, duplicatas por hash, limpeza aprovada e migração com reconferência de hash | 137 passed (19/11/2026) | Python, Microsoft Graph, SQLite, WebDAV | em uso |

Outros repositórios públicos: automações de relatório executivo e semanal, gerador de dossiês, índice de anexos,
remessa GRD, prestação de contas, índice de repositório jurídico, sync Google Calendar ↔ Notion, conversor UTM e
uma biblioteca de análise de vídeos. A lista completa está na aba Repositories.

### Como os projetos são construídos

O código é escrito com **Claude Code** e **Codex** como ferramentas, sob especificação e revisão minhas. Cada README
tem a seção "O que eu decidi × o que a IA gerou", e cada repositório traz `SANITIZACAO.md` (o que foi removido ou
trocado) e o comando de teste com o resultado registrado.

### Contato

Pelo GitHub: abra uma issue no repositório de interesse ou use as opções de contato deste perfil.

---

<a id="en"></a>
## English

I work in civil engineering, on a road-infrastructure program, and I build the tools that take repetitive document
work off the team: reports generated from their sources, SharePoint archives inventoried and made searchable,
dashboards that show where every number comes from. The repositories below are sanitized copies of those systems,
with fictitious data and tests that run without access to the real data.

### What I work on

- **Document automation**: Word/PDF reports built from scratch out of official spreadsheets and lists, validated before delivery.
- **Document systems and SharePoint**: inventory, deduplication and migration through Microsoft Graph, read-only whenever possible.
- **Applied AI and agents**: Claude Code and Codex as building tools, plus my own platform to govern agent-built projects.
- **Dashboards and data**: Python, FastAPI, DuckDB, React; every number on screen carries its provenance.
- **Engineering**: 4D BIM, critical path, UTM coordinates, transmittal and control of design documents.

### Featured projects

| Project | Problem → solution | Evidence | Stack | Status |
|---|---|---|---|---|
| [ai-project-os](https://github.com/Emmilymaciell/ai-project-os) | AI-built projects keep their state in the chat → platform that creates, versions, verifies and protects each project, with the repository as the source of truth | 375 engine `unittest` tests OK (2026-11-19); decisions in ADRs | Claude Code, Python (stdlib), PowerShell, Git hooks | in use |
| [infra-4d-intelligence](https://github.com/Emmilymaciell/infra-4d-intelligence) | The completion forecast for linear works comes from the contractor → independent recalculation from measured productivity, with a CPM engine, Monte Carlo and a 3D/4D viewer | 2,236 pytest tests passing, 6 skipped because they need a browser (2026-11-19); synthetic data | Python, FastAPI, IfcOpenShell, three.js | local demo |
| [cerebro-documental](https://github.com/Emmilymaciell/cerebro-documental) | Engineering archive on SharePoint with no inventory or search → deterministic pipeline that inventories, deduplicates, extracts text and indexes with page-level citations | 17 suites, 1726 PASS / 0 FAIL (2026-11-19); offline demo | Python, SQLite FTS5, Microsoft Graph | code ready; full run pending |
| [relatorio-tecnico-automatizado](https://github.com/Emmilymaciell/relatorio-tecnico-automatizado) | Monthly technical report made by copying last month's file → model reverse-engineered from published editions and a generator that builds the document from scratch, checked against the published PDF | 1068 passed (2026-11-19) | Python, python-docx, PyMuPDF, YAML | in use |
| [dashboard-juridico](https://github.com/Emmilymaciell/dashboard-juridico) | Legal archive only measurable by counting spreadsheet rows → read-only ingestion, analytical model with provenance, API and dashboard | 149 Python + 120 frontend tests (2026-11-19) | FastAPI, DuckDB, React, ECharts | in use |
| [organizacao-sharepoint](https://github.com/Emmilymaciell/organizacao-sharepoint) | SharePoint library over quota → cloud inventory without downloading files, hash-based duplicates, approved cleanup and migration with hash re-verification | 137 passed (2026-11-19) | Python, Microsoft Graph, SQLite, WebDAV | in use |

Other public repositories: executive and weekly report automations, dossier generator, annex index, document
transmittal (GRD), accountability reports, legal-repository index, Google Calendar ↔ Notion sync, UTM converter and a
video-analysis library. The full list is in the Repositories tab.

### How the projects are built

The code is written with **Claude Code** and **Codex** as tools, under my specification and review. Each README has a
section on what I decided versus what the AI generated, and each repository ships a `SANITIZACAO.md` (what was
removed or replaced) and the test command with its recorded result.

### Contact

Through GitHub: open an issue in the repository you are interested in, or use the contact options on this profile.
