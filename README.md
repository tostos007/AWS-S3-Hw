# DevOps Portfolio Website on AWS S3 for Tosin Sho

This is a simple DevOps portfolio website hosted on Amazon S3. Following Assignment 

## Steps I Took

### 1. Created the Website
- I made a basic HTML file called `index.html`
- It includes my name, skills, certifications, projects, and LinkedIn link

### 2. Created an S3 Bucket
- I created a new S3 bucket named `www.tosinsho.com`
- I turned on **static website hosting** in the bucket settings
- I set the index document to `index.html`

### 3. Uploaded My Website
- I uploaded my `index.html` file to the S3 bucket

### 4. Made the Bucket Public
- I added a **bucket policy** so anyone can view the site
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::www.tosinsho.com/*"
    }
  ]
}
