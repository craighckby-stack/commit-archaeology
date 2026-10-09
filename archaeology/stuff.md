# Emergent Repository Intelligence (stuff.md)

> Cross-commit patterns, architectural hotspots, and GLM-powered insights.

## Deterministic patterns

**Most-touched files (Architectural hotspots):**
- `docs/POSTMORTEMS.md` — 14 commits
- `prayers/bulk-prayers-1.json` — 11 commits
- `APPLICATIONS.md` — 9 commits
- `server.ts` — 9 commits
- `.gitignore` — 6 commits

**Files with iterative wrong->correct cycles (Hard-won lessons):**
- `server.ts` — 2 failed-and-fixed cycles
- `aetherforge-eval/expected-results/containment_metrics.json` — 1 failed-and-fixed cycles
- `src/engine/moralFilter.ts` — 1 failed-and-fixed cycles
- `APPLICATIONS.md` — 1 failed-and-fixed cycles
- `.env.example` — 1 failed-and-fixed cycles
- `firebase-blueprint.json` — 1 failed-and-fixed cycles
- `firestore.rules` — 1 failed-and-fixed cycles
- `src/components/HUD.tsx` — 1 failed-and-fixed cycles
- `src/core/auth/keyVault.ts` — 1 failed-and-fixed cycles
- `src/engine/darlekRAG.ts` — 1 failed-and-fixed cycles
- `src/engine/finalAuthority.ts` — 1 failed-and-fixed cycles
- `src/engine/modelConfig.ts` — 1 failed-and-fixed cycles
- `src/engine/physics.worker.ts` — 1 failed-and-fixed cycles
- `src/engine/prng.ts` — 1 failed-and-fixed cycles
- `src/engine/types.ts` — 1 failed-and-fixed cycles
- `src/engine/useAgentArchitect.ts` — 1 failed-and-fixed cycles
- `src/lib/github.ts` — 1 failed-and-fixed cycles

**Recurring themes in commit subjects (sampled across 68 total commits, deduplicated per commit):**
- `safety` — 4 commits (6% of total corpus)
- `improved` — 3 commits (4% of total corpus)
- `evaluation` — 3 commits (4% of total corpus)
- `readme` — 3 commits (4% of total corpus)
- `gemini` — 2 commits (3% of total corpus)
- `parsing` — 2 commits (3% of total corpus)
- `integrate` — 2 commits (3% of total corpus)
- `state` — 2 commits (3% of total corpus)

### 🎯 Semantic Retrieval & Embedding Priority Index (Vector Targets)
> High-churn / high-recovery files prioritized for vector embedding. These files yield the highest ROI for "have I broken this before" similarity queries.

1. `server.ts` — **Priority P0 (CRITICAL - Highest Fail/Fix Volume)** (2 fail-and-fixed recovery cycles)
2. `aetherforge-eval/expected-results/containment_metrics.json` — **Priority P1 (HIGH - Frequent Recovery Cycles)** (1 fail-and-fixed recovery cycles)
3. `src/engine/moralFilter.ts` — **Priority P1 (HIGH - Frequent Recovery Cycles)** (1 fail-and-fixed recovery cycles)
4. `APPLICATIONS.md` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)
5. `.env.example` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)
6. `firebase-blueprint.json` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)
7. `firestore.rules` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)
8. `src/components/HUD.tsx` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)
9. `src/core/auth/keyVault.ts` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)
10. `src/engine/darlekRAG.ts` — **Priority P2 (MEDIUM)** (1 fail-and-fixed recovery cycles)

---

## LLM-surfaced patterns (GLM)

**Architectural Hotspots and Recurring Failure Classes**

* **Model Configuration Instability**: The model cascade configuration appears to be a fragile area, requiring frequent adjustments. Commit [79134f60] shows a fix to reorder model priority and promote gemini-3.8-flash to primary, suggesting ongoing performance tuning issues.

* **ESLint Compatibility Issues**: Version conflicts with ESLint and @eslint/js led to a specific failure requiring a downgrade in commit [c00c5386], indicating dependency management challenges in the development environment.

* **Documentation Quality as Failure Point**: Two commits ([ba3fc29d], [feab7dec]) show documentation errors being introduced and subsequently fixed, with one commit incorrectly changing "a interactive" to "an interactive" in APPLICATIONS.md.

* **Security and Configuration Fragility**: Multiple commits ([e5283623], [2112f8b8]) focus on securing configuration and preventing credential exposure, suggesting this is a persistent concern requiring ongoing attention.

**Skill Growth or Evolution Visible Across Time**

* **Testing Infrastructure Development**: The project shows evolution from basic documentation to a comprehensive testing framework, evidenced by commits adding evaluation scripts ([ca702448]), behavioral tests ([80ef136f]), and containment tests ([f00889a8]).

* **Memory System Enhancement**: Early commits show basic functionality, while later commits ([19054438]) demonstrate integration of SHA-256 hashing for cryptographically chained state lineage, indicating maturation of the memory verification system.

* **Error Handling Maturation**: The progression from basic error handling to more sophisticated retry detection ([35b5ab59]) shows improvement in API interaction robustness.

* **Documentation Discipline**: The high frequency of documentation commits (DOCS type) suggests a growing emphasis on maintaining clear project documentation as the system complexity increases.

**Key Architectural Decisions and Hard-Won Lessons**

* **Separation of Concerns**: The project demonstrates a clear architectural decision to separate autonomous generative systems from verification systems, as documented in APPLICATIONS.md and reinforced through the moral filter implementation ([ef8378d4]).

* **Deterministic Approach**: Replacing Math.random() with a global PRNG ([2de91e08]) indicates a lesson learned about the need for deterministic behavior in testing and evaluation scenarios.

* **Security Layering**: The implementation of a moral triage gate before finalAuthority evaluation ([ef8378d4]) shows a hard-won lesson about the need for multiple safety layers in AI systems.

* **Repository Structure Evolution**: The transition from a generic repository structure to a more specialized AetherForge framework ([5454be26], [d832892a]) reflects a strategic decision to focus on frontier AI safety research.

* **Configuration Management Challenges**: The repeated issues with ESLint configuration and model settings suggest that the team has learned the importance of strict dependency versioning and configuration validation.