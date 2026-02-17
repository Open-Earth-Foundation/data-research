# AI / MCP Guidance for Data Research

This file helps AI assistants and MCP tools query and understand what we research. Read this first when answering questions about datasets, indicators, or structure.

## How to answer "What datasets do we have?"

Read `catalog/datasets.yaml`. It lists all datasets with id, name, publisher, description, coverage, themes, releases, and license (including commercial_use).

## How to answer "What datasets support city context / Chile / X use case?"

Read `collections/collections.yaml`. It groups datasets by geography and use case (e.g. `chile`, `core_city_context`).

## How to answer "What indicators does dataset X provide?" or "How do I get indicator Y?"

1. For the dataset: `reviews/{dataset_id}/releases/{version}/review.yaml` contains `key_indicators_used`.
2. For variable mapping: `review.yaml` includes `indicator_mapping` (or `indicator_to_variable`) with source variable names and value logic.
3. For sample outputs: `reviews/{dataset_id}/releases/{version}/sample/` — see `sample_files` in review.yaml for manifest.

## How to answer "Why do we use dataset X?" or "What are its strengths/limitations?"

Read `reviews/{dataset_id}/readme.md`.

## How to answer "Where is the sample data?" or "What files are in a release?"

Read `reviews/{dataset_id}/releases/{version}/review.yaml` — the `sample_files` section lists files and their purpose.

## How to answer "Can I use this dataset commercially?" or "What license does X have?"

Read `catalog/datasets.yaml` — each dataset has a `license` block with `id`, `url`, `commercial_use`, and optional `note`.

## Canonical paths

- **Catalog (all datasets):** `catalog/datasets.yaml`
- **Collections (groupings):** `collections/collections.yaml`
- **Dataset overview:** `reviews/{dataset_id}/readme.md`
- **Release details + indicator mapping:** `reviews/{dataset_id}/releases/{version}/review.yaml`
- **Sample data:** `reviews/{dataset_id}/releases/{version}/sample/`
- **Exploration notebooks:** `reviews/{dataset_id}/releases/{version}/notebook/`
