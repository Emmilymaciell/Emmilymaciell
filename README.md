# Emmily Maciel Corrêa Melo

**Engenharia civil · Automação documental · IA aplicada**
Goiânia, Brasil · [emmilymaciell.github.io](https://emmilymaciell.github.io)

[Português](#pt) · [English](#en)

<a id="pt"></a>
## Português

Estudante de Engenharia Civil na Universidade Federal de Goiás (UFG). Trabalho num programa de infraestrutura
rodoviária e construo as ferramentas que tiram o trabalho documental repetitivo das mãos da equipe: relatórios
gerados a partir das fontes, acervos no SharePoint inventariados e pesquisáveis, dashboards que mostram a origem de
cada número.

Os repositórios abaixo são cópias sanitizadas desses sistemas: dados fictícios ou sintéticos e testes que rodam sem
acesso ao dado real. Os números citados são resultados de teste registrados no README de cada repositório.

### Áreas

- **Automação documental** — relatórios Word/PDF montados do zero a partir de planilhas e listas oficiais, com validação antes da entrega.
- **Sistemas documentais e SharePoint** — inventário, deduplicação e migração pelo Microsoft Graph, em modo somente leitura sempre que possível.
- **IA aplicada e agentes** — Claude Code e Codex como ferramentas de construção, com uma plataforma própria para governar projetos feitos com agentes.
- **Dados e dashboards** — Python, FastAPI, DuckDB, React; cada número exibido carrega a sua proveniência.
- **Engenharia** — BIM 4D, caminho crítico, coordenadas UTM, remessa e controle de documentos de projeto.

### Projetos em destaque

**1. [ai-project-os](https://github.com/Emmilymaciell/ai-project-os)** — plataforma de governança de projetos feitos com IA
- **Problema:** projetos construídos com agentes guardam o estado na conversa, que se perde.
- **Solução:** plataforma que cria, versiona, verifica e protege cada projeto, com o repositório como fonte de verdade e decisões em ADRs.
- **Evidência:** 375 testes `unittest` do motor OK, 2 pulados (19/11/2026).
- **Tecnologias:** Claude Code, Python (stdlib), PowerShell, Git hooks · **Estado:** em uso

**2. [infra-4d-intelligence](https://github.com/Emmilymaciell/infra-4d-intelligence)** — previsão independente de término de obra linear
- **Problema:** a previsão de término vem de quem executa a obra.
- **Solução:** recálculo pela produtividade medida, com motor CPM, simulação Monte Carlo e visualizador 3D/4D.
- **Evidência:** 2236 testes pytest passando, 6 pulados por exigirem navegador, 0 falhas (19/11/2026); dados sintéticos.
- **Tecnologias:** Python, FastAPI, IfcOpenShell, three.js · **Estado:** demonstração local

**3. [cerebro-documental](https://github.com/Emmilymaciell/cerebro-documental)** — inventário e busca em acervo de engenharia
- **Problema:** acervo no SharePoint sem inventário nem busca.
- **Solução:** pipeline determinístico que inventaria, deduplica, extrai texto e indexa com citação de página.
- **Evidência:** 17 suítes, 1726 PASS / 0 FAIL (19/11/2026); demo offline.
- **Tecnologias:** Python, SQLite FTS5, Microsoft Graph · **Estado:** código pronto; execução em massa pendente

**4. [relatorio-tecnico-automatizado](https://github.com/Emmilymaciell/relatorio-tecnico-automatizado)** — relatório técnico mensal gerado do zero
- **Problema:** o relatório mensal era feito copiando o arquivo do mês anterior.
- **Solução:** modelo obtido por engenharia reversa das edições publicadas e gerador que monta o documento do zero, conferido contra o PDF publicado.
- **Evidência:** 1068 passed, 297 skipped por marcadores office/golden/network (19/11/2026).
- **Tecnologias:** Python, python-docx, PyMuPDF, YAML · **Estado:** em uso

**5. [dashboard-juridico](https://github.com/Emmilymaciell/dashboard-juridico)** — acervo jurídico com proveniência
- **Problema:** o acervo só era mensurável contando linhas de planilha.
- **Solução:** ingestão somente leitura, modelo analítico com proveniência, API e dashboard.
- **Evidência:** 149 testes Python passando, 1 pulado, e 120 testes de frontend (19/11/2026).
- **Tecnologias:** FastAPI, DuckDB, React, ECharts · **Estado:** em uso

**6. [organizacao-sharepoint](https://github.com/Emmilymaciell/organizacao-sharepoint)** — limpeza e migração de biblioteca SharePoint
- **Problema:** biblioteca SharePoint acima da cota.
- **Solução:** inventário pela nuvem sem baixar arquivos, duplicatas por hash, limpeza aprovada e migração com reconferência de hash.
- **Evidência:** 137 passed (19/11/2026).
- **Tecnologias:** Python, Microsoft Graph, SQLite, WebDAV · **Estado:** em uso

Outros repositórios públicos: automações de relatório executivo e semanal, gerador de dossiês, índice de anexos,
remessa GRD, prestação de contas, índice de repositório jurídico, sync Google Calendar ↔ Notion, conversor UTM e uma
biblioteca de análise de vídeos. Lista completa na aba Repositories e no [site](https://emmilymaciell.github.io).

### Como os projetos são construídos

O código é escrito com **Claude Code** e **Codex** como ferramentas, sob especificação e revisão minhas. Cada README
tem a seção "O que eu decidi × o que a IA gerou", e cada repositório traz `SANITIZACAO.md` (o que foi removido ou
trocado) e o comando de teste com o resultado registrado.

### Contato

Pelo GitHub: abra uma issue no repositório de interesse ou use as opções de contato deste perfil.

---

<a id="en"></a>
## English

Civil Engineering student at the Federal University of Goiás (UFG), Brazil. I work on a road-infrastructure program
and build the tools that take repetitive document work off the team: reports generated from their sources,
SharePoint archives inventoried and made searchable, dashboards that show where every number comes from.

The repositories below are sanitized copies of those systems: fictitious or synthetic data and tests that run
without access to the real data. Every number quoted is a test result recorded in that repository's README.

### Areas

- **Document automation** — Word/PDF reports built from scratch out of official spreadsheets and lists, validated before delivery.
- **Document systems and SharePoint** — inventory, deduplication and migration through Microsoft Graph, read-only whenever possible.
- **Applied AI and agents** — Claude Code and Codex as building tools, plus my own platform to govern agent-built projects.
- **Data and dashboards** — Python, FastAPI, DuckDB, React; every number on screen carries its provenance.
- **Engineering** — 4D BIM, critical path, UTM coordinates, transmittal and control of design documents.

### Featured projects

**1. [ai-project-os](https://github.com/Emmilymaciell/ai-project-os)** — governance platform for AI-built projects
- **Problem:** projects built with agents keep their state in the chat, where it gets lost.
- **Solution:** a platform that creates, versions, verifies and protects each project, with the repository as the source of truth and decisions in ADRs.
- **Evidence:** 375 engine `unittest` tests OK, 2 skipped (2026-11-19).
- **Stack:** Claude Code, Python (stdlib), PowerShell, Git hooks · **Status:** in use

**2. [infra-4d-intelligence](https://github.com/Emmilymaciell/infra-4d-intelligence)** — independent completion forecast for linear works
- **Problem:** the completion forecast comes from the contractor.
- **Solution:** recalculation from measured productivity, with a CPM engine, Monte Carlo simulation and a 3D/4D viewer.
- **Evidence:** 2,236 pytest tests passing, 6 skipped because they need a browser, 0 failed (2026-11-19); synthetic data.
- **Stack:** Python, FastAPI, IfcOpenShell, three.js · **Status:** local demo

**3. [cerebro-documental](https://github.com/Emmilymaciell/cerebro-documental)** — inventory and search for an engineering archive
- **Problem:** an engineering archive on SharePoint with no inventory or search.
- **Solution:** a deterministic pipeline that inventories, deduplicates, extracts text and indexes with page-level citations.
- **Evidence:** 17 suites, 1,726 PASS / 0 FAIL (2026-11-19); offline demo.
- **Stack:** Python, SQLite FTS5, Microsoft Graph · **Status:** code ready; full run pending

**4. [relatorio-tecnico-automatizado](https://github.com/Emmilymaciell/relatorio-tecnico-automatizado)** — monthly technical report built from scratch
- **Problem:** the monthly report was made by copying last month's file.
- **Solution:** a model reverse-engineered from the published editions and a generator that builds the document from scratch, checked against the published PDF.
- **Evidence:** 1,068 passed, 297 skipped by office/golden/network markers (2026-11-19).
- **Stack:** Python, python-docx, PyMuPDF, YAML · **Status:** in use

**5. [dashboard-juridico](https://github.com/Emmilymaciell/dashboard-juridico)** — legal archive with provenance
- **Problem:** the archive was only measurable by counting spreadsheet rows.
- **Solution:** read-only ingestion, an analytical model with provenance, an API and a dashboard.
- **Evidence:** 149 Python tests passing, 1 skipped, and 120 frontend tests (2026-11-19).
- **Stack:** FastAPI, DuckDB, React, ECharts · **Status:** in use

**6. [organizacao-sharepoint](https://github.com/Emmilymaciell/organizacao-sharepoint)** — SharePoint library cleanup and migration
- **Problem:** a SharePoint library over quota.
- **Solution:** cloud inventory without downloading files, hash-based duplicates, approved cleanup and migration with hash re-verification.
- **Evidence:** 137 passed (2026-11-19).
- **Stack:** Python, Microsoft Graph, SQLite, WebDAV · **Status:** in use

Other public repositories: executive and weekly report automations, dossier generator, annex index, document
transmittal (GRD), accountability reports, legal-repository index, Google Calendar ↔ Notion sync, UTM converter and a
video-analysis library. Full list in the Repositories tab and on the [website](https://emmilymaciell.github.io).

### How the projects are built

The code is written with **Claude Code** and **Codex** as tools, under my specification and review. Each README has a
section on what I decided versus what the AI generated, and each repository ships a `SANITIZACAO.md` (what was
removed or replaced) and the test command with its recorded result.

### Contact

Through GitHub: open an issue in the repository you are interested in, or use the contact options on this profile.
