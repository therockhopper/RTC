---
title: 'Ibm S3 Bucket Cors'
date: 2022-05-12T17:46:39-03:00
---

how to set up CORS to enable all origins to use GET

```
ibmcloud cos put-bucket-cors --bucket BUCKET_NAME --cors-configuration '{ "CORSRules": [ { "AllowedMethods": ["GET"], "AllowedOrigins": ["*"] } ] }'  --region us-east
```
