# lol-highlight-dataset

一個專為 **Moment Retrieval（關鍵時刻檢索）** 與 **Highlight Detection（精華片段偵測）** 任務所設計的資料集，內容來自《英雄聯盟》的職業電競賽事影片。

本資料集可用於視覺語言模型、多模態檢索與電競影片理解等研究領域。

---

## 📁 Dataset Structure


<details>
<summary>點此展開</summary>

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


## 📌 檔案說明

### 🔹 `Complex_query_data/`

內含敘事型複雜查詢語句，包含地圖位置、選手角色與團隊狀態等語意背景，設計用於評估需深度理解語意的 Moment Retrieval 任務。

### 🔹 `Simple_query_data/`

內含事件型精華查詢語句（例如「caps 擊殺 perkz」），適用於以擊殺事件為核心、語句形式較簡單的 Highlight Detection 任務。

### 🔹 `pretrain_data/`

包含以下內容：

features/：使用 SlowFast、BLIP、CLIP 預先萃取的 .npz 特徵檔

pretrain_output_final.jsonl：用於弱監督預訓練的生成資料

---

## 🧪 支援任務

- **Moment Retrieval (MR)**  
  輸入：敘事型語句查詢
  輸出：影片中最符合語意的開始與結束時間區間

- **Highlight Detection (HD)**  
  輸入：完整賽事影片
  輸出：根據預設指標（如重要性分數、敘事對應）預測出的精華片段時間區間

---

## 📄 授權條款

本資料集僅供學術研究使用。
未經書面授權禁止用於商業用途、資料再分發或爬蟲擷取。

---

## ✉️ 引用與聯絡方式

Maintainer: **Victor Wang**  
GitHub: [@victor-wang0125](https://github.com/victor-wang0125)

> If you use this dataset in your research, please cite the related publication or acknowledge the dataset in your work.
