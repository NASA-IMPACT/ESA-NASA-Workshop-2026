# Hands-on Session: Building Scalable AI EO Workflows 

Earth Observation FMs are widely available, but turning them into workflows that fit real tasks and constraints remains resource-intensive. This workshop focuses on modular EO workflows that make it easier to adapt foundation models and EO tools to your own tasks, datasets, and research goals.

---
## Overview
This hands-on session introduces EO embedding workflows, downstream adaptation, and scalable experimentation with TerraTorch and TerraTorch Iterate through interactive notebooks and real-world examples.

- Generate embeddings from pretrained EO foundation models 
- Train lightweight downstream decoders 
- Explore a forest disturbance monitoring workflow 
- Run scalable HPO/NAS experiments with TerraTorch Iterate


## What You Will Learn

- Flexible spatial and temporal EO embedding aggregation strategies
- Decoder-only downstream adaptation on precomputed embeddings 
- Zero-invasive experiment configuration with TerraTorch Iterate 
- Efficient experiment tracking and comparison

---

## Session Outline

**Planned duration:** 4 hours

| Part | Topic                                                    | Format | Time   |
|------|----------------------------------------------------------|--------|--------|
| 0 | Introduction and workshop overview                       | Slides | 10 min |
|  | **Part 1: EO Foundation Models and Embedding Workflows** |  |        |
| 1 | EO foundation models, embeddings, and TerraTorch basics  | Slides + setup | 15 min |
| 2 | Embedding generation and inspection with TerraTorch      | Notebook follow-along | 30 min |
|  | Buffer, troubleshooting, and break                       | Break | 15 min |
|  | **Part 2: Downstream Tasks with EO Embeddings**          |  |        |
| 3 | Downstream adaptation with EO embeddings                 | Slides | 10 min |
| 4 | Decoder training on precomputed embeddings               | Notebook follow-along | 20 min |
|  | **Part 3: Real-World EO Use Case**                       |  |        |
| 5 | Forest disturbance monitoring workflow                   | Intro + notebook demo | 60 min |
|  | Buffer, troubleshooting, and break                       | Break | 15 min |
|  | **Part 4: Scalable Experimentation with Iterate**        |  |        |
| 6 | TerraTorch Iterate and workflow configuration            | Slides | 10 min |
| 7 | Distributed HPO/NAS and experiment tracking              | Notebook follow-along | 40 min |
| 8 | Closing discussion and Q&A                               | Discussion | 15 min |


## Materials

- `requirements.txt`: Package list for the workshop environment.

**Hands-on material**:
- `01_TerraTorch_Embeddings/`: Notebook and sample YAML file for embedding generation.
- `02_TerraTorch_Downstream/`: Notebook and sample YAML file for downstream tasks.
- `03_Embed2Scale_Usecase/`: Notebook for data exploration and downstream workflows.
- `04_TerraTorch_Iterate/`: TerraTorch Iterate workflows for scalable experimentation.

---

### Workshop data — `03_Forest_Disturbance_Monitoring`

The forest-disturbance notebook reads a ~15 GB data bundle that ships
separately from this repo. Download and unzip it from the workshop S3
bucket before launching the notebook (~5 minutes total):

```bash
# Download and unzip the data for 03_Forest_Disturbance_Monitoring
# May take about 5 minutes in total
cd ~
aws s3 cp s3://enw-04241552-kx1nks-shared/data/workshop_bundle.zip .
unzip -q workshop_bundle.zip -d workshop_data
```

This produces `~/workshop_data/workshop_bundle/{data,audit}/`. The
notebook's Section 0 auto-detects this path on the SageMaker VM; see
the comments in the Setup cell to override via `WORKSHOP_DATA_ROOT` if
you unzipped the bundle elsewhere.

---

## References

- TerraTorch: <https://github.com/torchgeo/terratorch>
- TerraTorch embedding examples:
  <https://github.com/terrastackai/terratorch/tree/main/examples/embeddings>
- TerraTorch Iterate: <https://github.com/IBM/terratorch-iterate>
