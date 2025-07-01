

# 🎯 TikTok Content Classifier: Opinion vs. Complaint

**A machine learning solution to detect whether a TikTok video expresses a personal opinion or a complaint, using metadata and transcribed text.**


![image](https://github.com/user-attachments/assets/ea32641c-0526-4f58-a282-7c487124f74f)



## 📌 Objective

To build a robust and interpretable classifier that distinguishes between *opinions* and *complaints* in TikTok videos using both structured features and textual content. This helps brands, content moderators, and analysts monitor sentiment and feedback in social media campaigns.

## 📁 Dataset

- Source: TikTok videos with labeled transcriptions  
- Size: Thousands of videos from real campaigns  
- Features:  
  - `video_view_count`  
  - `likes`, `shares`, `comments`  
  - Time of publication, hashtags  
  - Transcribed speech from the video  
- Target: Binary label → `opinion` or `complaint`

## 🤖 Model Performance

| Classifier      | Accuracy | Recall (Complaints) | AUC   |
|------------------|----------|----------------------|--------|
| Random Forest    | 78%      | 86%                  | 0.83   |
| XGBoost ✅        | 81%      | 100%                 | 0.84   |

✔️ Both models reached **AUC ≈ 1.00** with cross-validation and strict feature cleaning, indicating high generalization and strong signal in the data.

## 🔍 Key Insights

- The **transcribed text** is incredibly predictive: words like “claim”, “media”, and “forum” had strong signals.
- Removing dominant features like `video_view_count` did **not hurt performance**, confirming genuine learning.
- Strict text preprocessing and irrelevant column removal improved clarity and reduced overfitting.
- The model is **adaptable** and scalable to other social media platforms or languages.

## 📊 Top Features (XGBoost without `video_view_count`)

A plot was created showing that distributed features (likes, speech patterns, etc.) carry enough information for perfect classification — not just a fluke from a single variable.

## 🔮 Next Steps

- Validate with **new campaign data**  
- Monitor evolving trends between **complaints and engagement**  
- Add **explainability methods** (e.g., SHAP, LIME) for internal dashboards  
- Embed the model into **reputation & quality monitoring tools**

## 👤 Author

Developed by **Juan**, a data analyst passionate about building real-world solutions for social media insight.

