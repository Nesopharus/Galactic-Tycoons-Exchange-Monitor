# TEAM WORKFLOW: Gemini + Claude + Ollama

## 1. Roles & Responsibilities
- **Gemini CLI (Orchestrator):** 
  - Zentrale Koordination, Strategie und Kommunikation.
  - Research, Planung (Research -> Strategy -> Execution Zyklus).
  - Git/GitHub Management (Branches, PRs, Commits).
  - Finale Verifizierung und Dokumentation.
- **Ollama (Local Specialist - qwen2.5-coder):**
  - **Triviale Code-�nderungen:** JSDoc, einfache Bugfixes, Boilerplate, CSS-Anpassungen, Readme-Updates.
  - Parallele Code-Reviews und Logik-Pr�fungen des Gemini-Plans.
  - Wird genutzt, um Quoten zu sparen, wenn lokale Rechenpower ausreicht.
- **Claude Code (Surgeon):**
  - **Komplexe Implementierungen** und tiefgreifendes Refactoring.
  - Strategische Architektur-�nderungen.
  - Arbeitet NUR auf Basis eines von Gemini erstellten Plans mit \"Surgical Context\".

## 2. The \"Surgical Context\" Rule
1. Gemini MUST NOT send the whole index.html unless necessary.
2. Gemini MUST identify exact line numbers for changes.
3. Gemini MUST provide snippets with ## SNIPPET markers in the context file.

## 3. The Lifecycle
1. **Gemini:** Research + Plan + GitHub Issue/Branch.
2. **Ollama:** Critique the Plan (Parallel turn) OR Implement trivial changes.
3. **Claude:** Implement complex changes using Surgical Context (User-triggered).
4. **Gemini + Ollama:** Parallel Verification of the diff.
- **Gemini:** PR Creation + Documentation + Usage Logging. **MANDATE:** Always use regular merge commits (`--no-ff`) instead of squashing to preserve a detailed history for automated changelogs.
- **Gemini:** **Cleanup Phase.** Run powershell _local/scripts/cleanup.ps1.

## 4. Performance Metrics
Log via powershell _local/scripts/log-task.ps1.
