# Multi-Entity Relationship Explanation

![License](https://img.shields.io/badge/license-[Your_License]-blue.svg)
![DOI](https://img.shields.io/badge/DOI-ComingSoon-lightgrey)

## Description

We introduce the dataset designed to clarify relationships between multiple entities as an essential task, given the rapidly growing number of entities across the web.
Our dataset includes over 9,400 entity sets, each containing 3 to 5 entities, along with textual descriptions of their relationships. 
Additionally, we extract Freebase KGs for each entity set using multi-hop expansion to gather supporting entities crucial for comprehensive explanations.

## Repository Structure

 * [data](./data)
   * [graphs](./data/graphs): This folder contains graphs of each entity set by its ID. Each row in the file contains a triplet in "head tail relation" format.
   * [entity-and-relation-mapping](./data/entity-and-relation-mapping)
     * [entity2id.txt](./data/entity-and-relation-mapping/entity2id.txt): This file contains the Freebase ID of an entity with its corresponding numerical ID.
     * [entity2name.txt](./data/entity-and-relation-mapping/entity2name.txt): This file contains the Freebase ID of an entity with its corresponding name.
     * [relation2id.txt](./data/entity-and-relation-mapping/relation2id.txt): This file contains the Freebase ID of a relation with its corresponding numerical ID.
   * [multi-entity-relation-explanation.json](./data/multi-entity-relation-explanation.json): This file contains the entity sets with the explanations.
 * [README.md](./README.md)

## Dataset Format

- Size: `30GB`
- Fields / Columns in `JSON` file:
  - `id` — sample id
  - `set` — in which set (train/dev/test) the sample belongs to
  - `entity_ids` — Freebase IDs of all entities in the set
  - `entity_names` — entity names for each entity in the set
  - `original` — the original explanation extracted from Wikipedia
  - `rule_refined` — the explanation that has been automatically refined based on rules
  - `llm_refined` — the explanation that has been refined by the LLM
 
## Citation
If you use this dataset in your research, please cite:
```bibtex
@inproceedings{TBD,
  title        = {Enhancing User Understanding of Entity Relationships with Knowledge Graphs: A Dataset for Multi-Entity Relationship Explanation},
  author       = {Wiradee Imrattanatrai, Makoto P. Kato, Ken Fukuda},
  year         = {2025},
  publisher    = {TBD},
  doi          = {TBD},
  url          = {TBD}
}
```
