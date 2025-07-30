# lol-highlight-dataset

A dataset for **Moment Retrieval (MR)** and **Highlight Detection (HD)** on professional *League of Legends* esports match videos.

This dataset supports research in vision-language models, multimodal retrieval, and esports video understanding.

---

## 📁 Dataset Structure


<details>
<summary>Click to expand</summary>

```
lol-highlight-dataset/
├── Complex_query_data/
│   ├── highlight_test_release.jsonl
│   ├── highlight_train_release.jsonl
│   ├── highlight_train_release_paraphrased_openai
│   ├── highlight_val_release.jsonl
│   └── features/
│       ├── blip_aug_text_features_openai/
│       ├── blip_features/
│       ├── blip_video_features/
│       ├── clip_aug_text_features_openai/
│       ├── clip_features/
│       ├── clip_text_features/
│       ├── features_openai/
│       └── slowfast_features/
│
├── Simple_query_data/
│   ├── highlight_train_release.jsonl
│   ├── highlight_train_release_paraphrased_openai
│   ├── highlight_val_release.jsonl
│   └── features/
│       ├── blip_aug_text_features_openai/
│       ├── blip_features/
│       ├── blip_video_features/
│       ├── clip_aug_text_features_openai/
│       ├── clip_features/
│       ├── clip_text_features/
│       ├── features_openai/
│       └── slowfast_features/
│
├── pretrain_data/
│   ├── pretrain_output_final.jsonl
│   └── features/
│       ├── blip_query_features/
│       ├── blip_video_features/
│       ├── clip_features/
│       ├── clip_query_features/
│       └── slowfast_features/

```
</details>


## 📌 File Descriptions

### 🔹 `Complex_query_data/`

Contains **manually written narrative queries** that include contextual elements such as map locations, player roles, or team status. Designed for evaluating **moment retrieval** under rich semantic understanding.

### 🔹 `Simple_query_data/`

Contains **event-based highlight queries** (e.g., "caps killed perkz") for **highlight detection tasks** focused on simpler sentence forms and kill-based saliency.

### 🔹 `pretrain_data/`

Includes:
- `features/`: `.npz` files containing **pre-extracted visual features** from SlowFast、BLIP and CLIP
- `pretrain_output_final.jsonl`: Generated data used for pretraining with weak supervision

---

## 🧪 Supported Tasks

- **Moment Retrieval (MR)**  
  Input: A narrative-style query  
  Output: A timestamp span (start/end time) in the video that best matches the query

- **Highlight Detection (HD)**  
  Input: Full-match video  
  Output: Predicted highlight-worthy segments based on predefined metrics (e.g., saliency, narrative match)

---

## 📄 License

This dataset is made available **for academic research only**.  
Commercial use, redistribution, or data scraping is prohibited unless with written permission.

---

## ✉️ Citation & Contact

Maintainer: **Victor Wang**  
GitHub: [@victor-wang0125](https://github.com/victor-wang0125)

> If you use this dataset in your research, please cite the related publication or acknowledge the dataset in your work.
