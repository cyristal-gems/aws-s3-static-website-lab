# Step 3 — Set Your Bucket Policy

To make your site public, apply this policy (replace YOUR-BUCKET-NAME):  

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
```

👉 This allows anyone to read your files, but not change them.
