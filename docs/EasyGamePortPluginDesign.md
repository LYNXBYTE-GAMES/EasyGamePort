# EasyGamePort Plugin Design

## Overview
EasyGamePort centralises automation guidance inside a Unity Editor window. The `EasyGamePortWindow` drives the experience: it shows an onboarding panel, renders the task backlog, and orchestrates task execution state. Tasks themselves come from `TodoTaskCatalog`, which supplies immutable descriptors with titles, summaries, step-by-step prompts, and scripted log output for the simulated runs.

## Architecture
- **Presentation layer (IMGUI):** `EasyGamePortWindow` handles layout, transitions, and keyboard navigation using Unity IMGUI and `AnimBool` for smooth expansion.
- **Task orchestration:** `TaskViewModel` instances manage per-task state, timed log playback, and repaint hooks so the UI updates without polling external systems.
- **Data source:** `TodoTaskCatalog` keeps the backlog definition in one place, making it easy to swap in real data or extend with new descriptors.
- **Extensibility hooks:** The execution pathway is isolated in `ExecuteTask`, giving a clear seam for wiring real automation agents or backend calls.

## Features
- Guided loading sequence with staged messaging that reflects the preparation steps.
- Introductory assistant copy that outlines capabilities and expected outcomes.
- Expandable task cards with runnable workflows, status chips, and streaming logs.
- Keyboard-friendly navigation for quick selection and execution.