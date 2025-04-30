## 🔑 Setting Up Google BigQuery Access with Service Account JSON

To enable reading from or writing to BigQuery using PySpark, follow these steps to generate and configure the required Google Cloud service account credentials.

### 📥 Step 1: Download the Service Account JSON Key

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Select your GCP project (top navigation bar).
3. Navigate to **IAM & Admin** → **Service Accounts** or go directly:  
   [https://console.cloud.google.com/iam-admin/serviceaccounts](https://console.cloud.google.com/iam-admin/serviceaccounts)
4. Click **"Create Service Account"**:
   - Give it a name (e.g., `spark-bigquery-access`)
   - Click **"Create and Continue"**
5. Grant the following roles:
   - `BigQuery Data Viewer` *(for read access)*
   - `BigQuery Data Editor` *(if you need write access)*
   - `BigQuery Job User`
6. Click **Done**
7. In the service account list, click the **three dots** next to your new account → **Manage Keys**
8. Click **"Add Key" → "Create new key"**
   - Select **JSON**
   - Click **Create** – this downloads a `.json` key file to your machine

> ⚠️ **Keep this key file secure. Do not commit it to version control.**

---

### ⚙️ Step 2: Configure Your Spark Job

Ensure your PySpark script references the JSON credentials:

```python
df = spark.read.format('bigquery') \
    .option('credentialsFile', '/path/to/key.json') \
    .option('parentProject', 'your-gcp-project-id') \
    .option('table', 'your_dataset.your_table') \
    .load()
