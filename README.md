# Project Architect

Skill reutilizavel para conduzir projetos de software do PRD a entrega, incluindo auditoria de repositorios existentes, governanca Git, proposta e encerramento de tarefas, e aprendizado metodologico aprovado pelo usuario.

**Versao:** 0.1.0 | **Entrypoint:** [SKILL.md](SKILL.md)

## Principios

- Questionar propostas com argumentos tecnicos, sem concordancia automatica.
- Antes de novas tarefas, explicitar ganho esperado, mecanismo, criterio de aceite e responsavel.
- Evitar burocracia e testes repetitivos sem risco concreto, sem eliminar controles essenciais.
- Preservar `main` como integracao aprovada; reduzir branches e PRs desnecessarias.
- Em cada entrega: relatar realizado, verificacao real, proxima acao, responsavel e bloqueios. Se o responsavel for o usuario, oferecer passo a passo.
- Auditar projetos existentes e propor ajuste minimo, sem sobrescrever regras especificas.
- Propor aprendizado baseado em evidencias; modificar a metodologia apenas apos aprovacao.

## Instalacao global no Codex - Windows (PowerShell)

Pre-requisitos: Git instalado e acesso HTTPS ao repositorio.

```powershell
$destino = Join-Path $HOME '.agents\skills\project-architect'
New-Item -ItemType Directory -Force (Split-Path $destino) | Out-Null
git clone https://github.com/jmAndradex/project_architect.git $destino
Test-Path (Join-Path $destino 'SKILL.md')
```

O ultimo comando deve retornar `True`. Se a pasta ja existir, nao execute `git clone` novamente; atualize-a com:

```powershell
git -C (Join-Path $HOME '.agents\skills\project-architect') pull --ff-only
```

## Instalacao global no Codex - WSL/Linux

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/jmAndradex/project_architect.git ~/.agents/skills/project-architect
test -f ~/.agents/skills/project-architect/SKILL.md && echo 'Skill instalada'
```

Para atualizar:

```bash
git -C ~/.agents/skills/project-architect pull --ff-only
```

O Windows e o WSL possuem perfis distintos; instale em ambos se usar o Codex nos dois ambientes. Reabra uma sessao do Codex apos instalar. A instalacao por usuario nao depende de o repositorio de trabalho estar em `jmAndradex` ou `juparana-dev`, mas o agente precisa de acesso ao codigo que analisara.

### Instalacao somente no projeto

Alternativamente, copie a pasta completa da Skill (com `SKILL.md`, `references/`, `assets/` e `agents/`) para `.agents/skills/project-architect/` dentro do repositorio de trabalho. Nao e necessario instalar a Skill em cada repositorio quando ela ja esta instalada globalmente para o mesmo usuario e ambiente.

## Como invocar

A Skill pode ser descoberta pela descricao de suas tarefas ou invocada explicitamente pelo nome `project-architect`.

**Novo projeto**

> Use a Project Architect para transformar esta ideia em escopo minimo, PRD, AGENTS.md e primeira task. Antes de cada task, declare ganho, mecanismo, aceite e responsavel.

**Projeto existente**

> Use a Project Architect para auditar este repositorio. Leia AGENTS.md, main, branches, PRs, CI e estado real. Proponha somente ajustes com ganho concreto, sem alterar nada ate delimitar o escopo.

**Desenvolvimento**

> Aplique a Project Architect nesta entrega. Reaproveite branch/PR apropriada, valide so os riscos necessarios e feche a task com entregue, evidencias, proxima acao e responsavel.

**Limpeza Git**

> Use a Project Architect para identificar branches obsoletas com provas de integracao. Preserve commits unicos e nao exclua nada sem autorizacao.

**Aprendizado**

> Analise as friccoes deste ciclo e proponha ate tres novas regras que aumentem velocidade, com evidencias e limites. Nao edite a metodologia sem minha aprovacao.

## Conteudo

- [SKILL.md](SKILL.md): politica principal e roteamento do fluxo.
- [references/engineering-rules.md](references/engineering-rules.md): engenharia, branches, SHA/release e testes proporcionais.
- [references/task-contract.md](references/task-contract.md): proposta e encerramento de tarefas.
- [references/existing-projects.md](references/existing-projects.md): auditoria e adequacao incremental.
- [references/learning-loop.md](references/learning-loop.md): propostas de aprendizado e versionamento.
- [references/artifacts.md](references/artifacts.md): criterios para PRD, SPEC, README e AGENTS.md.
- [assets/AGENTS.template.md](assets/AGENTS.template.md) e [assets/PRD.template.md](assets/PRD.template.md): modelos opcionais.

## Observacoes

- GitHub armazena a fonte; apenas publicar nao instala ou atualiza as copias locais do Codex.
- Instalacao no ChatGPT, quando disponivel, exige importar o pacote `skill.zip` pela biblioteca de Skills. A instalacao no Codex nao sincroniza automaticamente com ChatGPT.
- Nunca publique segredos, dados internos ou codigo de projetos privados neste repositorio publico. Regras de repositorios especificos e suas autorizacoes continuam validas.
- Integracao em `main` nao significa automaticamente deploy em producao.

Referencia oficial: https://developers.openai.com/api/reference/cli
