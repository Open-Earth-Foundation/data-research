# Data Research

Research datasets for city context indicators, vulnerability inputs, and emissions-related proxies. This repo documents data sources, their suitability for downstream products, and curated sample outputs.

## Purpose

- **Catalog** official and near-official datasets used for city-level context
- **Review** releases for data quality, coverage, and integration notes
- **Document** indicator definitions and variable mappings
- **Provide** sample data and exploration notebooks for validation

## Structure

| Path | Purpose |
|------|---------|
| `catalog/datasets.yaml` | Master index: all datasets with metadata, coverage, themes, licenses |
| `collections/collections.yaml` | Groupings by geography or use case |
| `reviews/{dataset_id}/` | Per-dataset docs and release reviews |
| `reviews/{dataset_id}/releases/{version}/` | Release-specific: review, sample, notebooks |

## Quick Start

**List all datasets and indicators:**
```bash
# Read the catalog
cat catalog/datasets.yaml
```

**Find datasets by use case:**
```bash
# See collections (e.g. Chile, core city context)
cat collections/collections.yaml
```

**Understand a specific dataset:**
1. `reviews/{dataset_id}/readme.md` — why we use it, strengths, limitations
2. `reviews/{dataset_id}/releases/{version}/review.yaml` — key indicators, variable mappings, integration notes
3. `reviews/{dataset_id}/releases/{version}/sample/` — sample data and dictionaries

## Licenses

Each dataset in `catalog/datasets.yaml` includes a `license` block with:
- `id` — Short identifier (e.g. CC-BY-4.0)
- `url` — Full license text
- `commercial_use` — Whether commercial use is permitted

Curated samples in this repo follow the upstream dataset license. Verify current terms at the publisher site before production use.
