# Real-Time Sales Data ETL & Visualization Pipeline using Google Cloud

This project demonstrates a fully automated data pipeline for ingesting, processing, and visualizing global sales data. It splits uploaded files by country, loads them into BigQuery, and presents live dashboards in Looker for real-time decision-making.

---

## 🚀 Project Overview

**Goal**: Build a scalable ETL pipeline that transforms raw sales data into actionable insights for identifying key markets and KPIs.

---

## 🔧 Tech Stack

- **Frontend & Ingestion**: Python Flask Web App  
- **Cloud Storage**: Google Cloud Storage (GCS)  
- **ETL & Processing**: Google Cloud Functions + BigQuery  
- **Transformation**: SQL queries in BigQuery  
- **Visualization**: Looker (Google Data Studio)

---

## 📈 Workflow

1. **File Upload**  
   - Users upload raw sales `.csv` via a Flask web interface.
   - Files are automatically sent to a GCS bucket.

2. **Cloud Storage & Trigger**  
   - A **Cloud Function** listens for finalized uploads in the bucket.
   - Triggered automatically, this function loads the data into BigQuery.

3. **BigQuery Processing**  
   - Sales data is cleaned, validated, and transformed using SQL.
   - Data is split by country, deduplicated, and enriched with calculated metrics (e.g., revenue, quantity sold).

4. **Dashboarding with Looker**  
   - Cleaned and enriched datasets are connected to Looker.
   - Multiple dashboards were created to visualize:
     - **Top Markets**
     - **Sales Trends**
     - **Product Performance**
     - **Revenue KPIs**

5. **Automation**  
   - The full process is serverless and automated via Google Cloud.
   - New uploads trigger an entire ETL cycle ending in updated dashboards.

---

## 📊 Sample Insights

- Identify top 5 countries by revenue
- Detect underperforming SKUs
- Track real-time sales growth trends
- Monitor customer segmentation

---

## 📁 File Structure (Key Files)

```
/flask-app/
    └── app.py                 # Web app for file upload
/gcs-function/
    └── main.py                # Cloud Function to load to BigQuery
/bigquery/
    └── transform_queries.sql  # SQL transformations and cleaning
/lookml/
    └── dashboard.lookml       # Looker dashboard schema (optional)
/country-splits/
    └── *.csv                  # Output files split by country
```

---

## ✅ Results

- ⚡ Real-time sales insights available on Looker dashboards
- 📉 Reduced manual reporting by 90%
- 🌎 Enabled localized decision-making with country-specific metrics

---

## 🧠 Lessons Learned

- End-to-end automation on GCP streamlines business reporting
- Real-time feedback loops increase responsiveness to market changes
- Designing for scalability upfront saves hours of manual effort later

---

## 📌 Future Improvements

- Add user authentication to the Flask app
- Integrate anomaly detection in sales trends using ML
- Schedule daily summarization jobs for executive reports

---

## 📬 Contact

For queries, reach out via [LinkedIn](https://www.linkedin.com/in/your-profile) or email.
