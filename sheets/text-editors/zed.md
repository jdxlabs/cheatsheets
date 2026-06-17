# Zed

Terminal Font : Jetbrains Mono :
https://www.jetbrains.com/lp/mono/

```
// Zed settings
//
// For information on how to configure Zed, see the Zed
// documentation: https://zed.dev/docs/configuring-zed
//
// To see all of Zed's default settings without changing your
// custom settings, run `zed: open default settings` from the
// command palette (cmd-shift-p / ctrl-shift-p)
{
  "buffer_line_height": {
    "custom": 1.45,
  },
  "agent_buffer_font_size": 11.0,
  "agent_ui_font_size": 11.0,
  "ui_font_family": ".ZedSans",
  "edit_predictions": {
    "mode": "eager",
  },
  "project_panel": {
    "dock": "left",
  },
  "cli_default_open_behavior": "existing_window",
  "telemetry": {
    "diagnostics": false,
    "metrics": false,
  },
  "session": {
    "trust_all_worktrees": true,
  },
  "terminal": {
    "font_family": "JetBrains Mono",
    "font_size": 10,
    "font_weight": 300,
    "flexible": false,
    "line_height": "standard",
    "shell": {
      "program": "wsl.exe",
    },
    "blinking": "on",
    "max_scroll_history_lines": 5000,
  },
  "autosave": {
    "after_delay": {
      "milliseconds": 1000,
    },
  },
  "buffer_font_family": "Consolas",
  "file_types": {
    "hcl": ["*.tf"],
    "toml": ["*.toml"],
  },
  "agent_servers": {
    "mistral-vibe": {
      "type": "registry",
    },
    "claude-acp": {
      "type": "registry",
    },
  },
  "base_keymap": "VSCode",
  "ui_font_size": 14,
  "buffer_font_size": 11.0,
  "theme": {
    "mode": "system",
    "light": "One Light",
    "dark": "Ayu Mirage",
  },
}
```
