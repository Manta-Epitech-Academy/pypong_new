# Competency paths (slash notation)

TOC hooks in `metadata.yaml` use structured **`competency`** objects. For **PROG**, the **canonical** observable path used by the competency API is slash-separated:

```text
PROG/01/A1/pypong/1
```

Same meaning: domain **PROG**, skill **01**, level **A1**, workshop project **pypong**, **`obs_index`** **1** (resolve bucket segment).

Generated file **`competency_paths.json`** in this directory maps each stable workshop key (same string shape as historical dot-codes, e.g. `PROG-01.A1.1`) to `slash_path`. Regenerate from the **competency-framework** repo:

```bash
cd /path/to/competency-framework
python3 scripts/export_pypong_cf_map.py
```

(`TRANS-*` keys are listed in the map JSON with a `kind` other than `prog` until a TRANS tree exists.)
