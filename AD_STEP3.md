# AD: Set Your Bucket Policy to Go Public

🌍 Want the world to see your website? Time to open the gates!

✔️ Go to the **Permissions** tab.  
✔️ Find **Bucket policy**, click **Edit**.  
✔️ Paste this magic JSON (replace `your-bucket-name` with your real bucket name!):

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
