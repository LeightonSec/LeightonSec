CLAUDE.md — LeightonSec
Security engineering research lab and public portfolio.
Every repo is a production tool, a portfolio piece, or active research. Nothing is throwaway.

Stack

Language: Python (primary), HTML/Jinja2 (frontends), Shell (automation)
Web framework: Flask
Database: SQLite via Flask-SQLAlchemy
AI: Anthropic Claude API (claude-haiku-4-5-20251001)
Environment: macOS, Python venvs per project
Version control: Git, SSH, GitHub


Architecture
Five layers. Understand which layer a repo sits in before touching it.
LayerPurposeRepos1 — Core EngineDetection foundationai-firewall2 — SOC ToolkitDetection and responsepcap-analyser, intel-pipeline, security-toolkit, incident-tracker3 — VisibilityIntegration and dashboardsunified-dashboard, intel-dashboard4 — GRCCompliance and governancenis2-vendor-risk-framework, mfa-coverage-tracker5 — ResearchOffensive and defensive AI security researchllm-honeypot, llm-redteam, dolphin-watch

Security Standards
These apply across every repo without exception.

API keys in .env only — never committed, never logged, never in responses
.env, venv/, __pycache__/, *.db, logs/, reports/, *.pcap always gitignored
Servers bound to 127.0.0.1 unless the tool's purpose explicitly requires otherwise
Input validation on all external input — max lengths, whitelists, sanitisation
No external network calls unless the tool's stated purpose requires it
Severity always strings: "CRITICAL", "HIGH", "MEDIUM", "LOW"
Never reduce security posture to fix a convenience problem


Code Conventions

Detection logic in its own module — never inline in Flask routes
Thresholds and config in named dicts at the top of the relevant module
Flask routes thin — logic delegated to modules
All API responses JSON
Logs structured — severity, type, timestamp, detail minimum
Every tool needs a solid README with setup steps and sample output


Commit Conventions

Present tense, imperative: Add rate limiting to /chat endpoint
Specific — what changed and why if not obvious
Never commit: API keys, .env files, database files, PCAP files, log files


Claude Code Rules
Always:

Read the repo-level CLAUDE.md before writing any code
Follow existing patterns — do not introduce new ones without reason
Run a security review pass before marking work complete
Update repo-level CLAUDE.md status after completing work
Update README if functionality changes

Never:

Commit or log secrets or environment variables
Expose servers beyond 127.0.0.1 without explicit instruction
Introduce new dependencies without checking if stdlib covers the need
Skip input validation on any external input
Reduce rate limits, dedup windows, or security thresholds
Break existing API contracts between tools