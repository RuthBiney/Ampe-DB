# Ampe Movement Dataset (Ampe-DB)

A structured multimodal dataset for paired rhythmic interaction analysis based on **Ampe**, a traditional Ghanaian game.

---

## Overview

The **Ampe Movement Dataset (Ampe-DB)** is a culturally grounded audiovisual dataset designed to support research in:

* Human movement analysis
* Human–human interaction modeling
* Rhythm and synchronization analysis
* Pose-based machine learning
* Embodied and culturally responsive AI

Unlike conventional action-recognition datasets that focus on solo performers, Ampe-DB captures **dyadic, face-to-face rhythmic interaction** between two players engaged in repeated jump–clap–step cycles.

The dataset includes synchronized:

* RGB video clips
* Audio signals
* 2D pose keypoints
* Annotations
* Metadata
* Quality validation logs

This repository contains the **dataset structure, processing pipeline, documentation, and benchmark definitions**.

---

## Authors

* **Ruth Biney Senior**
* **Isaac Aboah**

---

## Dataset Highlights

* Traditional Ghanaian gameplay context
* Paired interaction focus
* Outcome-driven labels
* Rhythm-aware annotations
* Benchmark-ready splits
* Research and educational use
* Culturally grounded AI resource

---

## Dataset Structure

```text
Ampe_Dataset/
│
├── videos/
│   ├── clips/
│   │   ├── left_left/
│   │   ├── left_right/
│   │   ├── right_left/
│   │   └── right_right/
│   │
│   ├── freestyle_fullgame/
│   └── skeleton_outputs/
│
├── keypoints_normalized/
├── annotations/
└── metadata/
```

---

## Data Modalities

### 1. Video

* Format: MP4
* Resolution: 1920×1080
* Frame Rate: 60 FPS
* Viewpoint: Fixed frontal view

### 2. Audio

Embedded or extracted audio capturing:

* clap peaks
* footstep timing
* vocal rhythm cues

### 3. 2D Skeleton Keypoints

* CSV format
* frame-level keypoints
* two players per frame
* confidence scores included
* normalized per video clip

Each processed clip is stored as an individual normalized CSV file.

Example:

```text
left_left_C001_normalized.csv
left_right_C002_normalized.csv
```

This per-video structure improves:

* scalability
* download efficiency
* machine learning workflows
* selective access

### 4. Annotations

Includes:

* movement type labels
* synchronization labels
* outcome labels
* temporal lag
* round boundaries

### 5. Metadata

Includes:

* session information
* clip properties
* recording conditions
* anonymized participant information

---

## Benchmark Tasks

Ampe-DB supports the following benchmark tasks:

### 1. Movement Type Classification

* left_left
* left_right
* right_left
* right_right

### 2. Synchronization Detection

* in_sync
* out_of_sync

### 3. Round Outcome Prediction

* left_win
* right_win
* draw

### 4. Continuous Synchronization Scoring

---

## Data Processing Pipeline

1. Raw video collection
2. Video refinement and segmentation
3. Skeleton extraction
4. Keypoint normalization
5. Annotation
6. Metadata generation
7. Quality validation
8. Benchmark split generation

---

## Access Policy

Ampe-DB follows a **controlled open-access model**.

The dataset is broadly available to researchers, students, educators, and creators, but access requires completion of a **usage agreement form**.

### Request Access

Users must provide:

* full name
* institutional affiliation
* contact email
* intended use
* project description
* agreement to terms of use

**Access Form:** *https://docs.google.com/forms/d/e/1FAIpQLSeq9bxHdipJDF2nhvckIwrTVcZ8j3PtDpLf0O9c-PpV4zbWgA/viewform?usp=publish-editor*

---

## Terms of Use

* non-commercial use only
* no redistribution of raw data
* proper citation required
* respect participant privacy
* respect cultural context

Commercial use requires written permission.

---

## Citation

### APA 7

Biney Senior, R., & Aboah, I. (2026). *Ampe Movement Dataset (Ampe-DB): A paired rhythmic interaction dataset for traditional African gameplay*. Ampe Research Project.

### BibTeX

```bibtex
@dataset{ampe_db_2026,
  title        = {Ampe Movement Dataset (Ampe-DB): A Paired Rhythmic Interaction Dataset for Traditional African Gameplay},
  author       = {Ruth Biney Senior and Isaac Aboah},
  year         = {2026},
  publisher    = {Ampe Research Project}
}
```

---

## Known Limitations

* 2D only (no depth axis)
* pose estimation noise in fast jumps
* moderate dataset scale
* environmental variation across sessions
* cultural scope currently centered on Ghanaian Ampe

---

## Recommended Use Cases

* action recognition
* synchronization modeling
* graph neural networks
* transformer-based sequence learning
* culturally grounded AI research
* embodied interaction studies

---

## License

This dataset is released for **research and educational use only**.

Suggested license:

**CC BY-NC 4.0** for dataset files  
**MIT License** for code and scripts

See the Terms of Use for full conditions.

---

## Acknowledgements

We acknowledge the participating players, communities, and collaborators who contributed to the development of Ampe-DB.

This work aims to support inclusive and culturally grounded AI research.

---

## Contact

For access, permissions, or collaboration inquiries:

**Ampe Research Project**

*Add project email / GitHub contact here*