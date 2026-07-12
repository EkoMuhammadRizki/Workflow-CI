# Tautan Docker Hub

Docker Hub Repository: [https://hub.docker.com/r/ekomuhammadrizki/smsml-eko-churn](https://hub.docker.com/r/ekomuhammadrizki/smsml-eko-churn)

## Cara Menjalankan Image dari Docker Hub

1. Download/Pull image dari Docker Hub:
   ```bash
   docker pull ekomuhammadrizki/smsml-eko-churn:latest
   ```

2. Jalankan container:
   ```bash
   docker run -d -p 5000:5000 --name telco-churn-api ekomuhammadrizki/smsml-eko-churn:latest
   ```
