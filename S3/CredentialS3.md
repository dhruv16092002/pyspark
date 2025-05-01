## ☁️ Accessing Amazon S3 with PySpark

This guide explains how to read from and write to Amazon S3 buckets using PySpark, and how to generate AWS access credentials.

---

### 🔐 Step 1: Create AWS Access Key and Secret

1. Go to the [AWS Console](https://console.aws.amazon.com/).
2. Navigate to **IAM** → **Users**
3. Select your user or create a new one.
4. Attach the following policy:
   - `AmazonS3ReadOnlyAccess` *(for read-only access)*
   - `AmazonS3FullAccess` *(for read/write access)*
5. Click **Security Credentials** tab → **Create access key**
6. Choose **Programmatic access**
7. Copy and securely save:
   - **Access Key ID**
   - **Secret Access Key**

> ⚠️ **Treat these like passwords. Do not commit them to Git.**

---

### ⚙️ Step 2: Configure Spark for S3 Access

Set your AWS keys using one of the following options:

#### Option A: In Spark Session

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("S3 Access") \
    .config("spark.hadoop.fs.s3a.access.key", "YOUR_AWS_ACCESS_KEY") \
    .config("spark.hadoop.fs.s3a.secret.key", "YOUR_AWS_SECRET_KEY") \
    .config("spark.hadoop.fs.s3a.endpoint", "s3.amazonaws.com") \
    .getOrCreate()
