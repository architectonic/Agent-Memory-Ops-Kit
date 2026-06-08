# Graphify

Graphify is an optional project-discovery accelerator for generating a queryable graph from source files, documentation, and other project artifacts.

Use it to help an agent understand a project faster. Do not treat its output as canonical truth.

## Use Case

Graphify can support project onboarding by producing derived artifacts such as:

```text
graph.html
GRAPH_REPORT.md
graph.json
```

These outputs can help an agent populate:

```text
templates/project_profile.md
templates/project_memory.md
```

## Required First Step: Configure Ignore Rules

Before running Graphify on any repository or knowledge vault, create and review ignore rules.

Ignore at minimum:

```text
.env
.env.*
*.pem
*.key
*.p12
*.pfx
secrets/
credentials/
private/
node_modules/
.git/
.DS_Store
```

For private operating-memory vaults, also ignore canonical memory and ontology files unless the run is explicitly meant to analyze them:

```text
AGENTS.md
START_HERE.md
memory_model.md
memory/
ontology/
knowledge/
identity/
goals/
decisions/
sources/private/
```

For public template repositories, protect framework-defining files from accidental rewrite or generated drift:

```text
AGENTS.md
START_HERE.md
repo_contract.md
memory_model.md
ontology/
roles/
skills/
runbooks/
templates/
```

## Operating Rule

Graphify may read project sources to create a derived discovery report.

Graphify output must not directly overwrite:

- ontology files;
- memory model files;
- role definitions;
- canonical decisions;
- source indexes;
- project profiles;
- project memory files.

An agent may use Graphify output as input when drafting those files, but the final files must be reviewed against source artifacts.

## Source Hierarchy

Treat Graphify output as a derived source aid.

```text
actual repository / docs
> Graphify report
> agent summary
> inference
```

When Graphify and source files disagree, trust the source files.

## Safe Workflow

1. Configure ignore rules.
2. Run Graphify only on the intended project scope.
3. Review generated outputs before committing them.
4. Use `GRAPH_REPORT.md` to identify architecture, terminology, and questions.
5. Fill `project_profile.md` and `project_memory.md` manually or through an agent review step.
6. Label uncertain conclusions as assumptions or open questions.
7. Do not commit generated graph outputs if they contain private, sensitive, or irrelevant material.

## ABKB-Style Onboarding Pattern

For a private project-memory vault:

```text
source repo
→ Graphify discovery report
→ project profile draft
→ project memory draft
→ source review
→ canonical project memory
```

The discovery report accelerates onboarding. It does not replace source review.

## Caveats

- Generated graphs can encode stale, inferred, or incomplete relationships.
- Large generated files can pollute small memory repos.
- Assistant config changes should be reviewed before commit.
- Query logs and generated reports may expose sensitive details.
- Private projects require stricter ignore rules than public projects.

## Good Fit

Use Graphify when:

- entering an unfamiliar repo;
- onboarding a project agent;
- mapping dependencies and terminology;
- finding candidate architecture questions;
- creating a first project profile draft.

## Poor Fit

Do not use Graphify as:

- canonical memory;
- a replacement for source review;
- an automatic ontology writer;
- an automatic decision recorder;
- a justification for committing generated artifacts blindly.
