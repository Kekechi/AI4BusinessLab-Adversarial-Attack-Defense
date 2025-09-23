# 📂 Data

This directory contains all machine-readable tagging data.

- **mapping.csv** → Spreadsheet-friendly dataset (exported from Google Sheets).
- **mapping.json** → Compiled master dataset (machine-readable).
- **json_group/** → Curated JSON files (approved, compiled into `mapping.json`).
- **json_individual/** → Individual JSON files, organized by contributor.

👉 Workflow:

1. Each member tags papers and saves their JSON under `json_individual/<name>/`.
2. During curation, agreed versions are copied into `json_group/`.
3. Run `scripts/compile_json.py` to rebuild `mapping.json`.
