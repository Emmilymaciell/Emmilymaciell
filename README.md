# Emmily Maciel Corrêa Melo

**Engenharia civil · Automação documental · Sistemas documentais · IA aplicada · BIM/4D**
Goiânia, Brasil · [emmilymaciell.github.io](https://emmilymaciell.github.io)

[Português](#pt) · [English](#en)

<a id="pt"></a>
## Português

Estudante de Engenharia Civil na Universidade Federal de Goiás (UFG). Trabalho num programa de infraestrutura
rodoviária e construo as ferramentas que tiram o trabalho documental repetitivo das mãos da equipe: relatórios
gerados a partir das fontes, acervos no SharePoint inventariados e pesquisáveis, dashboards que mostram a origem de
cada número. No lado de engenharia, desenvolvi uma plataforma de previsão independente de prazo para obras lineares,
com caminho crítico e BIM 4D.

Os repositórios abaixo são cópias sanitizadas desses sistemas: dados fictícios ou sintéticos e testes que rodam sem
acesso ao dado real. Cada número citado é resultado de teste ou medição do sistema real registrada no README do
repositório, sempre com data. Dos 18 repositórios públicos, 13 têm suíte automatizada e 5 têm execução ponta a ponta
registrada.

### Áreas

- **Automação documental** — relatórios Word/PDF montados do zero a partir de planilhas e listas oficiais, com validação antes da entrega.
- **Sistemas documentais e SharePoint** — inventário, deduplicação e migração pelo Microsoft Graph, em modo somente leitura sempre que possível.
- **IA aplicada e agentes** — Claude Code e Codex como ferramentas de construção, com uma plataforma própria para governar projetos feitos com agentes.
- **Dados e dashboards** — Python, FastAPI, DuckDB, React; cada número exibido carrega a sua proveniência.
- **Engenharia e BIM/4D** — caminho crítico, previsão de término, IFC, coordenadas UTM, remessa de documentos de projeto.

### Projetos em destaque

**1. [ai-project-os](https://github.com/Emmilymaciell/ai-project-os)** — plataforma de governança de projetos feitos com IA
- **Problema:** projetos construídos com agentes guardam o estado na conversa, que se perde.
- **Solução:** plugin do Claude Code e motor Python que criam, versionam, verificam e protegem cada projeto, com o repositório como fonte de verdade, revisores read-only e certificação de portabilidade por restauração isolada.
- **Papel:** concepção e decisões de arquitetura (19 ADRs); código gerado com Claude Code e Codex sob minha revisão.
- **Evidência:** 375 testes `unittest` do motor OK, 2 pulados (19/11/2026).
- **Tecnologias:** Claude Code, Python (stdlib), PowerShell, Git hooks · **Estado:** em uso

**2. [infra-4d-intelligence](https://github.com/Emmilymaciell/infra-4d-intelligence)** — previsão independente de término de obra linear
- **Problema:** a previsão de término vem de quem executa a obra, e a fiscalização não consegue recalculá-la.
- **Solução:** recálculo pela produtividade medida, com motor CPM próprio, Monte Carlo, Earned Schedule, IFC 4.3 e visualizador 3D/4D.
- **Papel:** especificação, decisões de produto e arquitetura (ADRs) e aceite; implementação com Claude Code e Codex.
- **Evidência:** 2236 testes pytest passando, 6 pulados por exigirem navegador, 0 falhas (19/11/2026); E2E Chrome 227 e Edge 231 PASS.
- **Tecnologias:** Python, FastAPI, IfcOpenShell, three.js · **Estado:** demonstração com dados sintéticos

**3. [cerebro-documental](https://github.com/Emmilymaciell/cerebro-documental)** — inventário e busca em acervo de engenharia
- **Problema:** acervo no SharePoint com 137.856 arquivos e 1,166 TB (inventário de 20/09/2026), sem inventário nem busca.
- **Solução:** pipeline determinístico que inventaria pela nuvem, deduplica por hash, extrai texto e indexa com citação de página; nenhuma IA no laço de processamento.
- **Papel:** decisões de escopo e arquitetura; código e auditorias de QA com Claude Code e Codex sob minha revisão.
- **Evidência:** 17 suítes, 1726 PASS / 0 FAIL (19/11/2026); demo offline.
- **Tecnologias:** Python, SQLite FTS5, Microsoft Graph · **Estado:** em evolução — processamento em massa ainda NO-GO

**4. [relatorio-tecnico-automatizado](https://github.com/Emmilymaciell/relatorio-tecnico-automatizado)** — relatório técnico mensal gerado do zero
- **Problema:** o relatório mensal de ~43 páginas era feito copiando o arquivo do mês anterior; 101 anomalias históricas catalogadas.
- **Solução:** modelo obtido por engenharia reversa de 14 edições publicadas e gerador que monta o documento do zero, conferido contra o PDF publicado.
- **Papel:** método e critérios de aceite; implementação com Claude Code e Codex sob minha revisão.
- **Evidência:** 1068 passed, 297 skipped por marcadores office/golden/network (19/11/2026); golden test do nº 14 com 43/43 páginas.
- **Tecnologias:** Python, python-docx, PyMuPDF, YAML · **Estado:** em uso

**5. [dashboard-juridico](https://github.com/Emmilymaciell/dashboard-juridico)** — acervo jurídico com proveniência
- **Problema:** o acervo só era mensurável contando linhas de planilha.
- **Solução:** ingestão somente leitura com snapshot por ciclo, modelo analítico com proveniência por campo, API e dashboard.
- **Papel:** regras de negócio e decisões de produto; implementação com Claude Code e Codex sob minha revisão.
- **Evidência:** 149 testes Python passando, 1 pulado, e 120 testes de frontend (19/11/2026).
- **Tecnologias:** FastAPI, DuckDB, React, ECharts · **Estado:** em uso

**6. [organizacao-sharepoint](https://github.com/Emmilymaciell/organizacao-sharepoint)** — limpeza e migração de biblioteca SharePoint
- **Problema:** biblioteca SharePoint acima da cota (1.384,20 GiB contra 1.024 GiB).
- **Solução:** inventário pela nuvem sem baixar arquivos, duplicatas por hash, limpeza aprovada e migração com reconferência de hash.
- **Papel:** regras de operação e decisões técnicas; scripts e testes com Claude Code e Codex sob minha revisão.
- **Evidência:** cota reduzida para 861,14 GiB (registro de 11/11/2026); 137 testes passando (19/11/2026).
- **Tecnologias:** Python, Microsoft Graph, SQLite, WebDAV · **Estado:** em uso

### Outros repositórios

- **Automação documental:** [relatorio-executivo-automatizado](https://github.com/Emmilymaciell/relatorio-executivo-automatizado) · [relatorio-semanal-automatizado](https://github.com/Emmilymaciell/relatorio-semanal-automatizado) · [gerador-de-dossies](https://github.com/Emmilymaciell/gerador-de-dossies) · [indice-anexos](https://github.com/Emmilymaciell/indice-anexos) · [criador-pastas-produtos](https://github.com/Emmilymaciell/criador-pastas-produtos) · [prestacao-contas-automacao](https://github.com/Emmilymaciell/prestacao-contas-automacao) · [engvoltaica-portfolio](https://github.com/Emmilymaciell/engvoltaica-portfolio)
- **Sistemas documentais:** [repositorio-juridico](https://github.com/Emmilymaciell/repositorio-juridico)
- **Engenharia:** [conversor-utm](https://github.com/Emmilymaciell/conversor-utm) · [remessa-grd](https://github.com/Emmilymaciell/remessa-grd)
- **IA aplicada e integrações:** [video-knowledge-lab](https://github.com/Emmilymaciell/video-knowledge-lab) · [calendar-sync-worker](https://github.com/Emmilymaciell/calendar-sync-worker)

Resumo de cada um no [site](https://emmilymaciell.github.io).

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
SharePoint archives inventoried and made searchable, dashboards that show where every number comes from. On the
engineering side, I built an independent schedule-forecast platform for linear works, with critical path
and 4D BIM.

The repositories below are sanitized copies of those systems: fictitious or synthetic data and tests that run
without access to the real data. Every number quoted is a test result or a measurement of the real system recorded
in that repository's README, always dated. Of the 18 public repositories, 13 have an automated test suite and 5 have
a recorded end-to-end run.

### Areas

- **Document automation** — Word/PDF reports built from scratch out of official spreadsheets and lists, validated before delivery.
- **Document systems and SharePoint** — inventory, deduplication and migration through Microsoft Graph, read-only whenever possible.
- **Applied AI and agents** — Claude Code and Codex as building tools, plus my own platform to govern agent-built projects.
- **Data and dashboards** — Python, FastAPI, DuckDB, React; every number on screen carries its provenance.
- **Engineering and 4D BIM** — critical path, completion forecasting, IFC, UTM coordinates, transmittal of design documents.

### Featured projects

**1. [ai-project-os](https://github.com/Emmilymaciell/ai-project-os)** — governance platform for AI-built projects
- **Problem:** projects built with agents keep their state in the chat, where it gets lost.
- **Solution:** a Claude Code plugin and Python engine that create, version, verify and protect each project, with the repository as the source of truth, read-only reviewers and portability certified by isolated restore.
- **Role:** concept and architecture decisions (19 ADRs); code generated with Claude Code and Codex under my review.
- **Evidence:** 375 engine `unittest` tests OK, 2 skipped (2026-11-19).
- **Stack:** Claude Code, Python (stdlib), PowerShell, Git hooks · **Status:** in use

**2. [infra-4d-intelligence](https://github.com/Emmilymaciell/infra-4d-intelligence)** — independent completion forecast for linear works
- **Problem:** the completion forecast comes from the contractor, and the supervisor cannot recompute it.
- **Solution:** recalculation from measured productivity, with a home-built CPM engine, Monte Carlo, Earned Schedule, IFC 4.3 and a 3D/4D viewer.
- **Role:** specification, product and architecture decisions (ADRs) and acceptance; implementation with Claude Code and Codex.
- **Evidence:** 2,236 pytest tests passing, 6 skipped because they need a browser, 0 failed (2026-11-19); E2E Chrome 227 and Edge 231 PASS.
- **Stack:** Python, FastAPI, IfcOpenShell, three.js · **Status:** demo on synthetic data

**3. [cerebro-documental](https://github.com/Emmilymaciell/cerebro-documental)** — inventory and search for an engineering archive
- **Problem:** a SharePoint archive of 137,856 files and 1.166 TB (inventory of 2026-09-20) with no inventory or search.
- **Solution:** a deterministic pipeline that inventories from the cloud, deduplicates by hash, extracts text and indexes with page-level citations; no AI inside the processing loop.
- **Role:** scope and architecture decisions; code and QA audits with Claude Code and Codex under my review.
- **Evidence:** 17 suites, 1,726 PASS / 0 FAIL (2026-11-19); offline demo.
- **Stack:** Python, SQLite FTS5, Microsoft Graph · **Status:** evolving — bulk processing still NO-GO

**4. [relatorio-tecnico-automatizado](https://github.com/Emmilymaciell/relatorio-tecnico-automatizado)** — monthly technical report built from scratch
- **Problem:** the ~43-page monthly report was made by copying last month's file; 101 historical anomalies catalogued.
- **Solution:** a model reverse-engineered from 14 published editions and a generator that builds the document from scratch, checked against the published PDF.
- **Role:** method and acceptance criteria; implementation with Claude Code and Codex under my review.
- **Evidence:** 1,068 passed, 297 skipped by office/golden/network markers (2026-11-19); golden test of edition 14 at 43/43 pages.
- **Stack:** Python, python-docx, PyMuPDF, YAML · **Status:** in use

**5. [dashboard-juridico](https://github.com/Emmilymaciell/dashboard-juridico)** — legal archive with provenance
- **Problem:** the archive was only measurable by counting spreadsheet rows.
- **Solution:** read-only ingestion with per-cycle snapshots, an analytical model with per-field provenance, an API and a dashboard.
- **Role:** business rules and product decisions; implementation with Claude Code and Codex under my review.
- **Evidence:** 149 Python tests passing, 1 skipped, and 120 frontend tests (2026-11-19).
- **Stack:** FastAPI, DuckDB, React, ECharts · **Status:** in use

**6. [organizacao-sharepoint](https://github.com/Emmilymaciell/organizacao-sharepoint)** — SharePoint library cleanup and migration
- **Problem:** a SharePoint library over quota (1,384.20 GiB against a 1,024 GiB limit).
- **Solution:** cloud inventory without downloading files, hash-based duplicates, approved cleanup and migration with hash re-verification.
- **Role:** operating rules and technical decisions; scripts and tests with Claude Code and Codex under my review.
- **Evidence:** quota down to 861.14 GiB (recorded 2026-11-11); 137 tests passing (2026-11-19).
- **Stack:** Python, Microsoft Graph, SQLite, WebDAV · **Status:** in use

### Other repositories

- **Document automation:** [relatorio-executivo-automatizado](https://github.com/Emmilymaciell/relatorio-executivo-automatizado) · [relatorio-semanal-automatizado](https://github.com/Emmilymaciell/relatorio-semanal-automatizado) · [gerador-de-dossies](https://github.com/Emmilymaciell/gerador-de-dossies) · [indice-anexos](https://github.com/Emmilymaciell/indice-anexos) · [criador-pastas-produtos](https://github.com/Emmilymaciell/criador-pastas-produtos) · [prestacao-contas-automacao](https://github.com/Emmilymaciell/prestacao-contas-automacao) · [engvoltaica-portfolio](https://github.com/Emmilymaciell/engvoltaica-portfolio)
- **Document systems:** [repositorio-juridico](https://github.com/Emmilymaciell/repositorio-juridico)
- **Engineering:** [conversor-utm](https://github.com/Emmilymaciell/conversor-utm) · [remessa-grd](https://github.com/Emmilymaciell/remessa-grd)
- **Applied AI and integrations:** [video-knowledge-lab](https://github.com/Emmilymaciell/video-knowledge-lab) · [calendar-sync-worker](https://github.com/Emmilymaciell/calendar-sync-worker)

A summary of each one is on the [website](https://emmilymaciell.github.io).

### How the projects are built

The code is written with **Claude Code** and **Codex** as tools, under my specification and review. Each README has a
section on what I decided versus what the AI generated, and each repository ships a `SANITIZACAO.md` (what was
removed or replaced) and the test command with its recorded result.

### Contact

Through GitHub: open an issue in the repository you are interested in, or use the contact options on this profile.
