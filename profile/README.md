## Hi there 👋 Welcome to **jazzydog-labs**

> _An open playground for AI-assisted, self-bootstrapping software development._

### 🧩 Why we exist
Modern LLMs are brilliant—but their context windows are finite and expensive.  
**jazzydog-labs** explores a modular, *autopoietic*-like workflow in which:

* Each repo is a **bounded context** with its own spec, contract, and rolling n-k-token summary.  
* Specialized AI agents (Synthesiser, Implementer, Critic, Observer) collaborate with humans, touching only the context they need.  
* The system continuously **re-summarises itself**, so new agents (or humans) can jump in without reading the whole codebase.

Think of it as continuous bootstrapping: the project *builds the process that builds the project, using the process built by the project*.

---

### 🏗️ Current architecture at a glance

| Layer | Repo | One-liner |
|-------|------|-----------|
| **Environment** | `foundry-bootstrap` | Canonical dot-files & toolchain – clone once, code anywhere. |
| **Orchestration** | `loom` | Weaves all sibling repos together; runs cross-repo commands. |
| **System registry** | `bill-of-materials` | Declarative graph of every repo, its type, status & dependencies. |
| **Design workspace** | `crucible` | AI-driven domain modelling; turns intent into `CONTRACT.yaml`. |
| **Code generation** | `forge` | Reads domain contracts, emits runnable scaffolds & tests. |
| **Artifact ledger** | `ledger` | Stores every prompt, response, diff & snapshot for auditability. |
| **Artifact & secret store** | `vault` | **Source of truth for generated schemas/clients/scaffolds** *plus* encrypted runtime secrets. |
| **Dev ergonomics** | `just-aliases` | Quality-of-life CLI shortcuts (`just test`, `just lint`, …). |

> **Walking skeleton**: `loom demo` clones → models → generates code → logs artifacts— all in one shot.

---

### 🔭 What’s next

| Theme | Draft repos / services | Goal |
|-------|------------------------|------|
| **Config domain** | `loom-config` | Dedicated bounded context for cross-repo config/versioning. |
| **Distributed BOM** | `.bom.yaml` in every repo | CI verifier to keep the graph live & accurate. |
| **Vault hardening** | `vault-agent` | Harden storage for **both** secrets *and* generated artifacts. |
| **Cost telemetry** | `token-meter` | Track per-agent token usage & latency; surface in Grafana. |
| **Prompt evolution** | `prompt-workbench` | Agents propose prompt changes; humans approve via PR. |

Have an idea? Open a discussion or draft a proposal in **`jazzydog-labs/rfcs`** (coming soon).

---

### 🌈 Contributing

1. **Fork & clone** the repo that interests you.  
2. Run `just bootstrap` (foundry-bootstrap does the heavy lifting).  
3. _TODO:_ Follow the local `CONTRACT.yaml` → tests should pass (`just test`). 
4. _TODO:_ Create a PR; the **Critic agent** will review alongside humans.  
5. Don’t sweat perfection—iterate! We’re as interested in the *process* as the code. We should reach coding-process-as-code asymptotically.

---

### 👩‍💻 Docs & resources

* **Architecture overview:** [`bill-of-materials/README.md`](https://github.com/jazzydog-labs/bill-of-materials)  
* **Design blueprints:** [`crucible/blueprints/`](https://github.com/jazzydog-labs/crucible/tree/main/blueprints)  
* **CLI cheatsheet:** [`just-aliases/README.md`](https://github.com/jazzydog-labs/just-aliases)  
* _TODO:_ **Process journal:** Each repo’s `/ledger/` directory (prompts, responses, diffs).

---

### 🍿 Fun facts

* The lab is named after **Jazz**, a very enthusiastic dog who never ships on Friday.  
* Our default breakfast is black coffee and unchecked ideas.  

---

> _“You can do mighty things with Markdown… and even mightier things with well-scoped prompts.”_

Happy hacking!  
— **jazzydog-labs**
