# Wonder Kid — 100% Completion and Phone QA Protocol

## Gate 1 — Grok

Target: 80–90% working implementation.

Grok builds and connects the V1 systems, integrates available assets, creates placeholders for missing production art, tests, fixes ordinary bugs, and produces a completion report.

Grok does not need to make every future feature or every final art asset.

## Gate 2 — Claude

Target: verified 100% of the defined V1 scope.

Claude does not rebuild the project. Claude performs complete integration and quality assurance.

Claude must:
- run all automated tests
- run integration/headless tests where practical
- inspect architecture end-to-end
- verify every core system is actually connected
- verify scenes and transitions
- verify save/load
- verify player and modular character
- verify Chanel
- verify animation state machines
- verify asset registry/imports
- verify adventure framework
- verify education/content data
- verify energy
- verify journal/world state
- verify settings and parent foundations
- verify two-player foundation where implemented
- verify error handling and recovery
- fix release-blocking issues within scope
- document non-blocking issues
- produce CLAUDE_FINAL_REVIEW.md

Claude may call the project READY FOR PHONE TEST only when there are no known release blockers for the defined V1 scope.

## Gate 3 — Phone

Phone testing is representative and risk-based.

Do not manually replay every level.

### Smoke test
- install
- launch
- loading
- orientation
- touch
- menus
- settings
- character
- Meadow
- movement
- interaction
- Chanel
- save
- exit
- relaunch
- load

### Representative gameplay
Test at least:
- one exploration/nature activity
- one engineering/physics activity
- one logic/reasoning activity
- one multi-step activity
- one cooking/math/budgeting activity when available
- one world-state-changing activity
- one two-player flow when available

Then rely on automated/integration tests for repeated framework-based content. Manually test any adventure that contains a unique system or unique code path.

## Definition of 100%

100% means the defined V1 architecture, systems, core flows, tests, save/load, asset integration, Chanel, Meadow, representative adventures, and release-critical error handling are complete and connected, with no known release blockers.

100% does not mean every future adventure, world, cosmetic, or expansion has been built.
