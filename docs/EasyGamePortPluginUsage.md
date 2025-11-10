# EasyGamePort Plugin Usage

## Installation
1. Copy the `Assets/Plugins/EasyGamePort` folder into your Unity project (Unity 2020.3 LTS or newer).
2. Ensure the files remain inside an `Editor` subfolder so they compile into the editor-only assembly.
3. Open Unity; the script will compile automatically.

> ℹ️ The folder layout mirrors Unity's desktop plug-in guidance and remains ready for future native bundles on macOS or other platforms [^unity-native].

[^unity-native]: Unity Technologies. "Building Plugins for Desktop Platforms." https://docs.unity3d.com/560/Documentation/Manual/PluginsForDesktop.html

## Opening the Plugin
- Navigate to `Window → EasyGamePort`.
- Dock the window wherever you prefer; Unity remembers the layout within the current workspace.

## Working with Tasks
- A brief staged loading sequence prepares the EasyGamePort catalog, showing progress such as initialization, structure analysis, and final checks.
- The introduction panel explains what the assistant can do; scroll below to browse the curated automation tasks.
- Use the mouse or arrow keys to highlight a task, press **Enter** to expand its guidance, then click **Execute** to simulate a run.
- Status chips (Idle, Running, Completed, Error) and streamed logs make it easy to follow progress without leaving the editor.

## Extending the Plugin
- Add or edit tasks inside the plugin to tailor workflows to your project.
- Replace the IMGUI layout with UI Toolkit if you need richer styling or responsive layouts.
- Connect a real backend agent by piping live progress updates into the existing task state and log hooks.
