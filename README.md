# ⚡ Linkup Plugin for Dify

This repository contains the source code for the **Linkup Search Plugin** for [Dify](https://dify.ai) — enabling real-time web search using the [Linkup](https://linkup.so) engine.

Provides real-time web and knowledge base search across public + premium sources with optional deep agentic search capabilities.

---

## 🛠 Initial Setup

To get started with plugin development, follow [Dify’s Plugin Development Docs](https://docs.dify.ai/plugins/quick-start/develop-plugins/initialize-development-tools).

### 1. Install the CLI and initialize the plugin:

```bash
./dify-plugin-darwin-arm64 plugin init
# or
dify plugin init
```
---
## 🧩 Plugin Structure

| Path                      | Purpose                                      |
|---------------------------|----------------------------------------------|
| `_assets/`                | Logo and visual assets for the plugin       |
| `provider/search_web.py` | Provider logic — handles credential setup   |
| `tools/search_web.py`    | Tool logic — implements the search function |
| `manifest.yaml`          | Plugin metadata and configuration           |
| `tools/search_web.yaml`  | Tool manifest with parameters and labels    |

---

## 🔧 Create a New Tool

To create an additional tool within the same plugin, follow:
👉 [Dify Tool Plugin Documentation](https://docs.dify.ai/plugins/quick-start/develop-plugins/tool-plugin)

You can define new functionality in the `tools/` folder and register it in `manifest.yaml`.

---

## 🧪 Debugging

To debug your plugin during development:

1. Go to [Dify Plugin Manager](https://cloud.dify.ai/plugins)
2. Click "Get debugging token" (top-right) and update it

```bash
cp .env.example .env
```

4. Run the plugin with:

```bash
python -m main
```

You’ll see logs and responses in your terminal as Dify invokes your plugin.

---

## 📦 Packaging

When ready to publish a new version:

1. Update the version field in:
   - `manifest.yaml`
   - `README.md`

2. Build the plugin package from the root directory:

```bash
dify plugin package ./src/search-web
```

This will generate a `.difypkg` file ready for commit.

---

## 🔐 Privacy & Data Use

This plugin may process personal data (such as IP addresses, queries, or contact data) as defined in the [Linkup Privacy Policy](https://linkup-platform.notion.site/Linkup-Privacy-Policy-197161ecef69800287c9cfca4bf1d39d). The plugin follows all applicable privacy regulations, including GDPR.

---
